# Employee Attrition Analyisis

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
- Google Collab

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
**Full Dashboard**

![](https://github.com/mariown/Belajar-Penerapan-Data-Science/blob/main/Full%20Dashboard.jpg)

**Attrition Filtered Dashboard**
![](https://github.com/mariown/Belajar-Penerapan-Data-Science/blob/main/Attrition%20Filtered)

### Interpretation :

#### **Analisis Dashboard Employee Attrition**



Dashboard ini menampilkan analisis atribut karyawan di perusahaan, dengan fokus pada faktor-faktor yang mempengaruhi tingkat attrisi atau pengunduran diri karyawan. Berikut adalah interpretasi dari setiap bagian dashboard:

**Key Metrics**

- **Total Employee:** 179
- **Attrition:** 16.92%
- **Average Monthly Income:** $4.9K
- **Average of Employees:** 33
- **Average of Total Working Years:** 8

**Persentase Karyawan Berdasarkan Level Jabatan**

Mayoritas karyawan berada di level jabatan rendah.

**Jumlah Karyawan Berdasarkan Perjalanan Bisnis**

Karyawan yang tidak melakukan perjalanan bisnis dan yang sering melakukan perjalanan bisnis hampir seimbang.

**Distribusi Job Involvement**

Mayoritas karyawan memiliki tingkat keterlibatan kerja yang tinggi.

**Jarak Tempuh Karyawan ke Tempat Kerja**

Sebagian besar karyawan tinggal dalam jarak 10-20 km dari tempat kerja.

**Tingkat Kepuasan Lingkungan Kerja**

Tingkat kepuasan lingkungan kerja bervariasi dengan mayoritas karyawan memiliki kepuasan tinggi.

**Distribusi Stock Option Level**

Sebagian besar karyawan tidak menerima stock options.

**Tingkat Keseimbangan Kerja-Hidup**

Sebagian besar karyawan menilai keseimbangan kerja-hidup mereka sebagai baik.

**Tingkat Kepuasan Pekerjaan**

Mayoritas karyawan memiliki tingkat kepuasan pekerjaan yang tinggi atau sangat tinggi.

**Distribusi Masa Kerja Karyawan**

Banyak karyawan yang bekerja kurang dari 5 tahun, namun ada juga yang bekerja lebih dari 10 tahun.

**Masa Kerja Karyawan dengan Manajer**

Sebagian besar karyawan bekerja dengan manajer mereka selama 0-5 tahun.

**Variabel Utama yang Mempengaruhi Status Attrisi**

Faktor-faktor penting yang mempengaruhi attrisi termasuk jarak dari rumah, umur, dan kepuasan lingkungan kerja.

### Insight Rangkuman

1. **Konsentrasi Karyawan di Level Rendah:** Mayoritas karyawan berada di level jabatan rendah, menunjukkan fokus pada peran operasional. Perusahaan perlu mengevaluasi jalur pengembangan karir untuk memastikan adanya peluang peningkatan.

2. **Perjalanan Bisnis:** Karyawan yang sering bepergian memiliki risiko lebih tinggi terhadap attrisi. Mengurangi frekuensi perjalanan atau menawarkan insentif dapat meningkatkan kepuasan dan retensi.

3. **Keterlibatan Kerja yang Tinggi:** Tingkat keterlibatan kerja yang tinggi menunjukkan komitmen yang kuat, namun penting untuk memantau tanda-tanda burnout dan memastikan keseimbangan kerja-hidup.

4. **Jarak Tempuh:** Jarak tempuh yang panjang dapat meningkatkan ketidakpuasan karyawan. Pertimbangkan kebijakan kerja fleksibel atau dari rumah untuk mengurangi stres perjalanan.

5. **Kepuasan Lingkungan Kerja:** Kepuasan yang tinggi perlu dipertahankan melalui program peningkatan lingkungan kerja.

6. **Stock Options:** Menawarkan stock options dapat menjadi insentif kuat untuk retensi, terutama untuk posisi strategis.

7. **Keseimbangan Kerja-Hidup:** Menjaga keseimbangan kerja-hidup adalah kunci retensi jangka panjang. Perusahaan perlu terus mengembangkan program pendukung keseimbangan ini.

8. **Kepuasan Pekerjaan:** Tingkat kepuasan kerja yang tinggi berkontribusi pada retensi yang lebih baik. Program-program yang ada perlu dipertahankan dan ditingkatkan.

9. **Masa Kerja:** Program onboarding yang lebih baik dan mentoring dapat meningkatkan retensi awal karyawan.

10. **Masa Kerja dengan Manajer:** Rotasi manajer yang tinggi dapat mempengaruhi stabilitas tim. Program pengembangan kepemimpinan diperlukan untuk memastikan manajer tetap berada dalam posisi lebih lama dan membangun hubungan baik dengan tim.

[Link Dashboard](http://localhost:3000/public/dashboard/43d515a8-38cf-467b-88b3-017cdbdae7e8)


## Conclusion

#### Interpretasi Koefisien Regresi Logistik

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

