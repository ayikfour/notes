# **REKAYASA PERANGKAT APLIKASI BERGERAK**

## **CH. III. CONTEXT AWARE**

#### **DEFINISI**

terdapat dua tipe aplikasi:

- `static application`
- `dynamic application`
  perilaku app berdasarkan konteks.

aplikasi dinamik dibagi menjadi dua:

- berdasarkan `user input`
- berdasarkan `konteks` awareness

> context awareness merupakan kondisi dimana **_perangkat dapat merasakan situasi dimana aplikasi tersebut sedang digunakan_**.

definisi ahli:

> konsep dari **_memanfaatkan informasi untuk meningkatakn kualitas interaksi. menggunakan lokasi, kehadiran, social untuk memprediksi kebutuhan user_**. - Gartner.

contohnya:

> pengingat ulang tahun pasangan. ketika melewati toko bunga aplikasi akan mengirimkan notifikasi reminder ulang tahun.

**konteks**

> _sebuah informasi yang dapat digunkaan untuk mengenali suatu kondisi/situasi dari sebuah entitas_

---

#### KEUNTUNGAN DAN BATASAN

pengembangan `masih dalam tahap awal`.

`sensor` dibutuhkan untuk menentukan `konteks`.

##### TIPE SENSOR

- `motion/location`
  seperti gps, akselero, gyro, infrared.
- `environmental`
  thermal, kelembapan, angin dll.
- `physicological`
  grip, pulse, skin temperature.

##### BATASAN

- terbatasnya kemampuan sensor dalam memproses informasi.
- bandwith jaringan yang kecil.
- kemampuan terbatas perangkat.
- konteks berganti dengan cepat.
- isu keamanan.

#### KEUNTUNGAN

desainer dapat memanfaatkan informasi konteks untuk mendapatkan dapat yang berkorelasi saja.

misalkan:

    seseorang tidak akan merasa terganggu jika disediakan daftar barang kesukaan yang sedang diskon.

---

#### JENIS KONTEKS

- location based
- time based
- user state based
- application based
- network based
- history

---

#### PERALATAN

1. Google awareness API
2. Aware
3. SenseIot
