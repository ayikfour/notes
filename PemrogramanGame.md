# PEMROGRAMAN GAME

### **Game engine**
> software yang dapat dikembangkan dan digunakan untuk sebagai dasar pengembangan game lainnya tanpa banyak modifikasi. - *Jason Gregory* 

berikut adalah perkembangan game engine:
- hanya dapat digunakan untuk satu aplikasi saja.
- dapat dikembangkan untuk beberapa game serupa
- dapat digunakan untuk mengembangkan game secara spesifik dalam satu genre


### **Game Loop**

user input -> network -> game logic -> sound -> rendering.

### **Pseudo Code Game Loop**

```c++
TargetFrametime = 1000 / targetFramerate
while game is running
    realDeltaTime = time since last frame	
    gameDeltaTime = realDeltaTime * gameTimeFactor	
    foreach Updateable o in GameWorld.updateableObjects	
        o.Update(gameDeltaTime)
    loop	
        foreach Drawable o in GameWorld.drawableObjects	o.Draw()
    loop	
        while (time spent this frame) < targetFrameTime 
    loop
loop 
```


# MATH FOR GAME

### **Vector**
#### penambahan:
>jika vektor berlawanan (**a** berlawanan dengan **b**) kemudian mencari resultan (garis tengah, **c**).
```
c = a + b = (ax + bx, ay + by, az + bz)
```

![gambar penambaha](/image/addition.png)

#### pengurangan:
>jika vektor berlawanan (**a** berlawanan dengan **b**) kemudian mencari jarak (garis **a** ke **b** yaitu **c**).
```
c = b - a = (bx -ax, by - ay, az -bz) 
```
![gambar pengurangan](/image/substract.png)

#### panjang vektor:
```
||a|| = akar(ax2 + ay2 + az2)
```

#### perkalian skalar:
```
s.a = (s.ax, s.ay, s.az)
```

#### dot product
- ***dot product digunakan untuk mencari panjang atau sudut***.
- hasil dari dot product adalah angka.

untuk mencari hasil perkalian dot. kita bisa menggunakan 2 cara
yang pertama dengan perkalian dot tiap komponen (x,y,z)

```
a.b = ax.bx + ay.by + az.bz
```
atau bisa juga dengan perkalian sudut.
alpha adalah sudut antara vector a dan b.
```
a.b = ||a||.||b||.cos(alpha)
```

#### cross product
- dot product digunakan untuk mencari vector ketiga. misal ada vector a dan b, hasil dari cross product adalah vector c.
- hasil dari cross product adalah vector lain.
- cross product menggunakan ***kaidah tangan kanan***
- posisi vector a dan b mempengaruhi hasil (vector c) positif atau negatif nya.

![gambar cross product 1](/image/crossproduct.png)
![gambar cross product dan kaidah tangan kanan](/image/crossproduct2.png)


# GAME GRAPHIC PT. 1

***openGL mentransformasi data 3D menjadi 2D***. karena monitor/layar kita menerima data 2D.

proses transformasi diatur oleh Graphic Pipeline. graphic pipeline mentransform 3D -> 2D, kemudian 2D -> Color pixel.

alur dari pipeline.
- Vertex shader 
- shape assembly
- geometry shader
- rasterization
- fragment shader
- test and blending

openGL modern setidaknya memiliki ***Vertex Shader*** dan ***Fragment Shader***

### **Vertex Data**
vertex merupakan kumpulan dari vertices. atau kumpulan dari data setiap koordinat 3D

openGL menggunakan 3D coordinate (x, y, dan z). masing masing menggunkan nilai dengan rentang

>-1.0 -> 1.0\
>disebut juga dengan\
>**Normalized Device Coordinate (NDC)**

kode dibawah menghasilkan Segitiga.
```C++
float vertices[] = {
    // X     Y      Z
    -0.5f,  -0.5f,  0.0f,
     0.5f,  -0.5f,  0.0f,
     0.0f,   0.5f,  0.0f
}; 
```
![gambar cross product 1](/image/vertices.png)

### **Shader In/Out**
dalam graphic pipeline, output dari setiap stage dibutuhkan untuk stage berikutnya. misalkan output dari ***vertex shader*** menjadi input dari ***fragment shader***.

seperti yang telah dideskripsikan sebelumnya (Graphic pipeline). hanya tiga komponen saja yang dapat kita inject shader. yaitu ***vertex***, ***geometry***, dan ***fragment shader***.

dengan syarat nama dan tipe harus sama. misal:
```C
//Vertex shader
#version 330 core
layout (location = 0) in vec3 aPos; 

out vec4 vertexColor; // specify a color output to the fragment shader

void main()
{
    gl_Position = vec4(aPos, 1.0); 
    vertexColor = vec4(0.5, 0.0, 0.0, 1.0); 
}
```

variable vertexColor menjadi input di fragment shader:

```C
#version 330 core
out vec4 FragColor;
  
in vec4 vertexColor; // the input variable from the vertex shader (same name and same type)  

void main()
{
    FragColor = vertexColor;
} 
```

### Uniform
cara lain passing data dari aplikasi (CPU) ke shaders (GPU) adalah menggunakan uniform. ***uniform bersifat global dan dapat diakses pada stage apapun dalam graphic pipeline***.

berikut contoh deklarasi Uniform type pada fragment shader:
```C
#version 330 core
out vec4 FragColor;
  
uniform vec4 ourColor; // Uniform type

void main()
{
    FragColor = ourColor;
}   
```

kemudian kita dapat memanggil uniform dan mengupdatenya:

```C 
float timeValue = glfwGetTime();
float greenValue = sin(timeValue) / 2.0f + 0.5f;
int vertexColorLocation = glGetUniformLocation(shaderProgram, "ourColor");
glUniform4f(vertexColorLocation, 0.0f, greenValue, 0.0f, 1.0f);
```

