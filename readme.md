
---

## 🧩 Rumus Rotasi Jarum Detik

### **Rumus**

```
((seconds / 60) * 360) + 90
```

### **Deskripsi**

Menghitung sudut rotasi jarum detik berdasarkan nilai detik saat ini, dengan tambahan offset agar posisi awal jarum sejajar dengan arah jam 12.

### **Parameter**

| Nama      | Tipe   | Deskripsi                    |
| --------- | ------ | ---------------------------- |
| `seconds` | Number | Nilai detik saat ini (0–59). |

### **Langkah Perhitungan**

1. `seconds / 60` → Mengubah detik menjadi proporsi dari satu putaran penuh.
2. `* 360` → Mengonversi proporsi menjadi derajat rotasi jam.
3. `+ 90` → Menambahkan offset agar posisi awal jarum berada di atas untuk offset kan `transform: rotate(90deg);`.

### **Nilai Kembali**

| Jenis           | Deskripsi                                          |
| --------------- | -------------------------------------------------- |
| Number (Degree) | Sudut rotasi jarum detik terhadap pusat lingkaran. |

### **Catatan**

Offset `+90` digunakan karena rotasi 0° pada sistem CSS dimulai dari arah kanan (jam 3), bukan dari atas (jam 12).


---

Berikut versi **dokumentasi singkat** untuk penjelasan kodingan rotasi jarum menit dan jam 👇



## 🕒 Rumus Rotasi Jarum Menit dan Jam

### **Jarum Menit**

```
((minute / 60) * 360) + ((seconds / 60) * 6) + 90
```

### **Deskripsi**

Menghitung sudut rotasi jarum menit berdasarkan menit dan detik saat ini.
Tambahan `(seconds / 60) * 6` digunakan agar jarum menit bergerak halus setiap detik.

### **Parameter**

| Nama      | Tipe   | Deskripsi                    |
| --------- | ------ | ---------------------------- |
| `minute`  | Number | Nilai menit saat ini (0–59). |
| `seconds` | Number | Nilai detik saat ini (0–59). |

### **Nilai Kembali**

| Jenis           | Deskripsi                                          |
| --------------- | -------------------------------------------------- |
| Number (Degree) | Sudut rotasi jarum menit terhadap pusat lingkaran. |

### **Catatan**

Offset `+90` digunakan agar posisi awal jarum berada di atas (arah jam 12).

---

### **Jarum Jam**

```
((hour / 12) * 360) + ((minute / 60) * 30) + 90
```

### **Deskripsi**

Menghitung sudut rotasi jarum jam berdasarkan jam dan menit saat ini.
Tambahan `(minute / 60) * 30` membuat jarum jam bergerak perlahan setiap menit.

### **Parameter**

| Nama     | Tipe   | Deskripsi                    |
| -------- | ------ | ---------------------------- |
| `hour`   | Number | Nilai jam saat ini (0–23).   |
| `minute` | Number | Nilai menit saat ini (0–59). |

### **Nilai Kembali**

| Jenis           | Deskripsi                                        |
| --------------- | ------------------------------------------------ |
| Number (Degree) | Sudut rotasi jarum jam terhadap pusat lingkaran. |

### **Catatan**

* Offset `+90` digunakan karena rotasi 0° dimulai dari arah kanan (jam 3).
* Tambahan `(minute / 60) * 30` memastikan posisi jarum jam akurat di antara dua angka jam.
