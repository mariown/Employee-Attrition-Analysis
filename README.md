# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

**Latar Belakang Perusahaan**

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. 

Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

Untuk mencegah hal ini semakin parah, manajer departemen HR ingin meminta bantuan untuk mengidentifikasi berbagai faktor yang mempengaruhi tingginya attrition rate tersebut. Selain itu, ia juga meminta untuk dibuatkan business dashboard untuk membantunya memonitori berbagai faktor tersebut. 
### Permasalahan Bisnis

#### 1. Tingginya Tingkat Attrition
Jaya Jaya Maju mengalami tingkat attrition yang lebih dari 10%, yang berarti banyak karyawan yang keluar dalam periode waktu tertentu. Hal ini menimbulkan biaya tambahan untuk rekrutmen dan pelatihan karyawan baru.

#### 2. Identifikasi Faktor-faktor Penyebab Attrition
Manajemen kesulitan untuk mengidentifikasi faktor-faktor utama yang menyebabkan karyawan keluar, seperti ketidakpuasan terhadap gaji, kurangnya peluang pengembangan karir, atau lingkungan kerja yang tidak kondusif.

### Cakupan Proyek

#### 1. Menjalankan Seluruh Proses dalam Proyek Data Science
Melakukan seluruh proses dalam proyek data science mulai dari pemahaman bisnis, pemrosesan data, analisis eksploratif data, pembuatan model machine learning, hingga deployment.

#### 2. Membuat Business Dashboard
Membuat business dashboard untuk membantu departemen HR dalam memahami data dan memonitor berbagai faktor yang mempengaruhi tingginya tingkat attrition.

### Persiapan

Sumber data: [Jaya Jaya Maju](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

Setup environment:
- Google COlab

```
import numpy
import pandas
import matplotlib
import seaborn
import sklearn
import statsmodels
import plotly
import scipy
import imblearn
from google.colab import drive
drive.mount('/content/drive')
```
- Metabase
```
from sqlalchemy import create_engine

URL = "postgresql://postgres.axwpbvulqapkfdafulgk:winayaario678@aws-0-ap-southeast-1.pooler.supabase.com:6543/postgres"

engine = create_engine(URL)
df.to_sql('Attrition Data', engine)
```
```
Host : aws-0-ap-southeast-1.pooler.supabase.com
Database name : postgres
Port : 6543
User : postgres.axwpbvulqapkfdafulgk
```

## Business Dashboard

Jelaskan tentang business dashboard yang telah dibuat. Jika ada, sertakan juga link untuk mengakses dashboard tersebut.

## Conclusion

#### Interpretasi Koefisien Regresi Logistik: HR Analytics

Berdasarkan grafik di atas, dapat diinterpretasikan hubungan antara berbagai faktor karyawan dengan kemungkinan keluarnya karyawan dari perusahaan.

**Variabel Dependen:** Attrition (0 = Menetap, 1 = Keluar)

- **Koefisien Positif:** Meningkatkan peluang attrition (keluar)
- **Koefisien Negatif:** Menurunkan peluang attrition (tetap)

#### Interpretasi per Variabel

1. **Age (Usia):**
   - Koefisien negatif (-0.279963) menunjukkan bahwa semakin tua usia karyawan, semakin kecil kemungkinannya untuk keluar dari perusahaan.

2. **DistanceFromHome (Jarak Rumah ke Tempat Kerja):**
   - Koefisien positif (0.291344) menunjukkan bahwa semakin jauh jarak rumah ke tempat kerja, semakin besar kemungkinannya untuk keluar dari perusahaan.

3. **MonthlyIncome (Gaji Bulanan):**
   - Koefisien positif (1.049603) menunjukkan bahwa semakin tinggi gaji bulanan, semakin besar kemungkinannya untuk keluar dari perusahaan. Ini mungkin counter-intuitive, namun bisa jadi karyawan dengan gaji tinggi mendapat tawaran menarik dari perusahaan lain.

4. **TotalWorkingYears (Total Tahun Bekerja):**
   - Koefisien negatif (-0.298440) menunjukkan bahwa semakin lama karyawan bekerja, semakin kecil kemungkinannya untuk keluar dari perusahaan.

5. **YearsAtCompany (Tahun di Perusahaan):**
   - Koefisien positif (0.656754) menunjukkan bahwa semakin lama karyawan berada di perusahaan, semakin besar kemungkinannya untuk keluar dari perusahaan. Ini mungkin perlu diinvestigasi lebih lanjut, apakah ada faktor tertentu yang menyebabkan karyawan senior keluar setelah lama bekerja.

6. **YearsInCurrentRole (Tahun di Jabatan Sekarang):**
   - Koefisien negatif (-0.236787) menunjukkan bahwa semakin lama karyawan berada di jabatan sekarang, semakin kecil kemungkinannya untuk keluar dari perusahaan.

7. **YearsWithCurrManager (Tahun dengan Manager Sekarang):**
   - Koefisien negatif (-0.872843) menunjukkan bahwa semakin lama karyawan bekerja dengan manager sekarang, semakin kecil kemungkinannya untuk keluar dari perusahaan. Hubungan yang kuat terindikasi dengan nilai koefisien absolut yang besar.

8. **BusinessTravel (Perjalanan Bisnis):**
   - Koefisien negatif (-0.484941) menunjukkan bahwa karyawan yang sering melakukan perjalanan bisnis lebih kecil kemungkinannya untuk keluar.

9. **EnvironmentSatisfaction (Kepuasan Lingkungan Kerja):**
   - Koefisien negatif (-0.531981) menunjukkan bahwa karyawan yang puas dengan lingkungan kerja lebih kecil kemungkinannya untuk keluar.

10. **JobInvolvement (Keterlibatan dalam Pekerjaan):**
    - Koefisien negatif (-0.809543) menunjukkan bahwa karyawan yang lebih terlibat dalam pekerjaan lebih kecil kemungkinannya untuk keluar. Hubungan yang kuat terindikasi dengan nilai koefisien absolut yang besar.

11. **JobLevel (Level Jabatan):**
    - Koefisien negatif (-1.159977) menunjukkan bahwa semakin tinggi level jabatan karyawan, semakin kecil kemungkinannya untuk keluar. Hubungan yang kuat terindikasi dengan nilai koefisien absolut yang besar.

12. **JobRole (Jabatan):**
    - Koefisien negatif (-0.004484) sangat mendekati nol, sehingga sulit disimpulkan. Mungkin perlu investigasi lebih lanjut.

13. **JobSatisfaction (Kepuasan Kerja):**
    - Koefisien negatif (-0.541815) menunjukkan bahwa karyawan yang puas dengan pekerjaan lebih kecil kemungkinannya untuk keluar.

14. **MaritalStatus (Status Pernikahan):**
    - Koefisien negatif (-0.253194) menunjukkan bahwa karyawan yang sudah menikah lebih kecil kemungkinannya untuk keluar.

15. **OverTime (Lembur):**
    - Koefisien positif (1.468370) menunjukkan bahwa karyawan yang sering lembur lebih besar kemungkinannya untuk keluar. Hubungan yang kuat terindikasi dengan nilai koefisien absolut yang besar.

16. **StockOptionLevel (Level Stock Option):**
    - Koefisien negatif (-1.394485) menunjukkan bahwa karyawan dengan level stock option yang lebih tinggi lebih kecil kemungkinannya untuk keluar. Hubungan yang kuat terindikasi dengan nilai koefisien absolut yang besar.

17. **WorkLifeBalance (Keseimbangan Hidup dan Kerja):**
    - Koefisien negatif (-0.614759) menunjukkan bahwa karyawan yang memiliki keseimbangan hidup dan kerja yang lebih baik lebih kecil kemungkinannya untuk keluar.

### Kesimpulan:

Tabel koefisien regresi logistik ini memberikan gambaran tentang berbagai faktor yang memengaruhi kemungkinan attrition karyawan.

**Faktor yang meningkatkan peluang attrition:**
- Jarak rumah ke tempat kerja
- Gaji Bulanan
- Tahun di Perusahaan
- OverTime

**Faktor yang menurunkan peluang attrition:**
- Usia
- Total Tahun Bekerja
- Tahun di Jabatan Sekarang
- Tahun dengan Manager Sekarang
- Perjalanan Bisnis
- Kepuasan Lingkungan Kerja
- Keterlibatan dalam Pekerjaan
- Level Jabatan
- Kepuasan Kerja
- Status Pernikahan
- Level Stock Option
- Keseimbangan Hidup dan Kerja


## Rekomendasi Action Items
- Meninjau kembali beban kerja dan memastikan distribusi tugas yang adil agar work life balnce karyawan terjaga.
- Meningkatkan kondisi lingkungan kerja fisik, seperti ruang kerja yang nyaman, fasilitas rekreasi, dan area istirahat yang memadai.
- Mendorong komunikasi yang terbuka dan transparan antara manajer dan karyawan.
- Melakukan peninjauan kebijakan stock option saat ini dan membandingkannya dengan praktik terbaik di industri untuk memastikan daya saing.

