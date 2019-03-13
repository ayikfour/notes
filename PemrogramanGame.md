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
penambahan:
>jika vektor berlawanan (**a** berlawanan dengan **b**) kemudian mencari resultan (garis tengah, **c**).
```
c = a + b = (ax + bx, ay + by, az + bz)
```

![gambar penambaha](/image/addition.png)

pengurangan:
>jika vektor berlawanan (**a** berlawanan dengan **b**) kemudian mencari jarak (garis **a** ke **b** yaitu **c**).
```
c = b - a = (bx -ax, by - ay, az -bz) 
```
![gambar penambaha](/image/substract.png)