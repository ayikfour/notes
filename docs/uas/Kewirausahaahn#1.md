# **ANALISIS BISNIS DAN STUDI KELAYAKAN BISNIS**

Terdapat dua studi atau analisis yang dapat digunakan:

- Studi kelayakan usaha
- Analisis SWOT

Dari hasil studi tersebut dapat digunakan untuk:

- merintis usaha baru
- mengembangkan usaha
- memilih jenis usaha/investasi

Pihak pihak yang memerlukan dan berkepentingan:

- pihak wirausahawan: `untuk mengetahui kelayakan bisnis`
- pihak investor: `untuk mengetahui jenis investasi yang tepat`
- pihak masyarakat dan pemerintah: `sebagai bahan kajian untuk mengetahui manfaat usaha untuk masyarakat`

## **PROSES DAN TAHAPAN STUDI KELAYAKAN**

1. Tahap penemuan ide
2. Tahap formulasi tujuan (visi/misi)
3. Tahap analisis
   1. Aspek pasar
   2. Aspek teknik produksi/operasi
   3. Aspek manajemen/pengilahan
   4. Aspek finansial
4. Tahap keputusan (`Dilaksanakan/tidak`)

#### ANALISIS KELAYAKAN

1. Analisis aspek pemasaran
   - kebutuhan dan keinginan konsumen
   - segmentasi pasar
   - target
   - nilai tambah
   - masa hidup produk
   - struktur pasar
   - persaingan pasar dan strategi
   - ukuran pasar
   - pertumbuhan pasar
   - laba kotor
   - pangsa pasar
2. Analisis aspek produksi/operasi
   - lokasi operasi
   - volume operasi
   - mesin dan peralatan
   - bahan baku
   - tenaga kerja
   - tata letak
3. Analisis aspek manajemen/pengolahan
   - kepemilikan
   - organisasi
   - tim manajemen
   - karyawan
4. Analisis finansial
   - kebutuhan dana
   - sumber dana
   - proyeksi neraca
   - proyeksi laba rugi
   - proyeksi aliran kas

#### PROYEKSI ALIRAN KAS

terdapat 3 aliran kas:

- kas masuk: `penerimaan berupa hasil penjualan/pendapatan`
- kas keluar: `biaya yang dikeluarkan`
- kas masuk bersih: `selisih kas masuk dan kas keluar`

proyeksi aliran kas masuk bersih:

```javascript
aliran_kas_masuk = laba_setelah_pajak + penyusutan + (1 - tarif_pajak) * bunga;
```

## **KRITERIA INVESTASI**

kriteria investasi untuk mengetahui layak atau tidaknya suatu investasi. terdapat beberapa metode:

- payback period
- net present value
- internal rate of return
- probability index

<br>

#### PAYBACK PERIOD

periode yang diperlukan untuk menutup kembali pengeluaran investasi. berikut adalah rumus:

```javascript
periode_pembayaran_kembali = nilai_sekarang/kas_masuk_bersih * 1 tahun
```

**misal:**
suatu perusahaan menanamkan modalnya dalam bentuk investasi 48.000.000 kemudian diperoleh keunrungan setelah pajak senilai 10.000.000 dan depresiasi sebesar 16.000.000. maka:

```javascript
periode_pembayaran_kembali = 48.000.000 / (10.000.000 + 6.000.000) * 1 tahun
periode = 3 tahun.
```

**dengan catatan:**

- **profit** = penerimaan total tahunan - biaya tahunan yang dikeluarkan (Co + Ct)
- **Co**= biaya tetap awal
- **Ct** = biaya variable

<br>

#### NET PRESENT VALUE

untuk menghitung interest rate dan nilai bersih:

`NPV = sum(PF * Ct) - sum(PF * Bt)`

`PF = (1 + tingkat_bunga)`<sup>-1</sup>

- PF: Faktor nilai. misal. **bunga bank** yang berlaku **18%** dan perode waktu **1 thun**. maka:
  > `PF = (1 + 0.18)`<sup>-1</sup>
  >
  > `PF = 0.847`
- Bt: benefit/keuntungan
- Ct: biaya total

**Misal:** perusahaan konveksi di bandung ingin menambah mesin jahit. biaya investasi awal adalah 40jt. umur dari mesin jahit adalah 5 tahun. dari hasil durvey didapat perkiraan aliran khas sebagai berikut:

| Tahun | Ct (total) | Bt (penerimaan) |
| ----- | ---------- | --------------- |
| 0     | 40         | 0               |
| 1     | 10         | 20              |
| 2     | 15         | 25              |
| 3     | 40         | 80              |
| 4     | 20         | 60              |
| 5     | 5          | 40              |

dengan bunga = 0.18. didapati sebagai berikut:

| Tahun | PF    | Ct  | Bt  | PF x Ct | PF x Bt | NPV   |
| ----- | ----- | --- | --- | ------- | ------- | ----- |
| 0     | 1     | 40  | 0   | 40.00   | 0       | -4    |
| 1     | 0.847 | 10  | 20  | 8.47    | 16.95   | 8.48  |
| 2     | 0.718 | 15  | 25  | 10.77   | 17.95   | 7.18  |
| 3     | 0.606 | 40  | 80  | 24.34   | 46.69   | 22.35 |
| 4     | 0.515 | 20  | 60  | 10.34   | 30.95   | 20.63 |
| 5     | 0.437 | 5   | 40  | 2.19    | 17.48   | 15.29 |
