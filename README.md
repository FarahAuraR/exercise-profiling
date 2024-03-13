## Module 5
**Farah Aura Rosadi - 2206824773 - Pemrograman Lanjut B** <br>

### Hasil dari uji JMeter dengan GUI
* **HTTP Request untuk `/all-student`:**
  [![temp-Image-D0q-Pc8.avif](https://i.postimg.cc/mDwxhnX2/temp-Image-D0q-Pc8.avif)](https://postimg.cc/jwL3FMYG)

* **HTTP Request untuk `/all-student-name`:**
  [![temp-Imaget-TJwgp.avif](https://i.postimg.cc/ryj0LF97/temp-Imaget-TJwgp.avif)](https://postimg.cc/XXZ7fWmg)

* **HTTP Request untuk `/highest-gpa`:**
  [![temp-Image-RM08og.avif](https://i.postimg.cc/W18TdhdP/temp-Image-RM08og.avif)](https://postimg.cc/jDDG9q68)

### Hasil uji JMeter dengan CLI
* **HTTP Request untuk `/all-student`:**
  [![temp-Image-Fvkv-Na.avif](https://i.postimg.cc/cJ1Y3gT7/temp-Image-Fvkv-Na.avif)](https://postimg.cc/ZWgCtqG0)

* **HTTP Request untuk `/all-student-name`:**
  [![temp-Image-VKfv7s.avif](https://i.postimg.cc/gjtB9bJQ/temp-Image-VKfv7s.avif)](https://postimg.cc/bSbRbM19)

* **HTTP Request untuk `/highest-gpa`:**
  [![temp-Imagesb8p-IE.avif](https://i.postimg.cc/D01d6VG1/temp-Imagesb8p-IE.avif)](https://postimg.cc/CnLqMQmK)

### Profiling & Performance Optimization
**HTTP Request untuk `/all-student`:** <br>
1. Sebelum Optimisasi:
   [![temp-Imageqp-FIa-T.avif](https://i.postimg.cc/4dztrDfP/temp-Imageqp-FIa-T.avif)](https://postimg.cc/ZB5CNDyv)

2. Setelah Optimisasi:
- Profiling
  [![temp-Imagek-PIgi-A.avif](https://i.postimg.cc/XqRRpyS4/temp-Imagek-PIgi-A.avif)](https://postimg.cc/N2xJnFjz)
- JMeter
  [![temp-Image-APjwb-F.avif](https://i.postimg.cc/5N97S3gT/temp-Image-APjwb-F.avif)](https://postimg.cc/bdM9z1K9)

**HTTP Request untuk `/all-student-name`:** <br>
1. Sebelum Optimisasi:
   [![temp-Imager90h-JR.avif](https://i.postimg.cc/zv4yvpGv/temp-Imager90h-JR.avif)](https://postimg.cc/tntqm3PG)

3. Setelah Optimisasi:
- Profiling
  [![temp-Image-Twq8bx.avif](https://i.postimg.cc/4xPhb68L/temp-Image-Twq8bx.avif)](https://postimg.cc/K1KzmMhB)
- JMeter
  [![temp-Imagefj-MT8-C.avif](https://i.postimg.cc/P55qHB4y/temp-Imagefj-MT8-C.avif)](https://postimg.cc/bs4PHV4S)

**HTTP Request untuk `/highest-gpa`:** <br>
1. Sebelum Optimisasi:
   [![temp-Imagee-Aq-GYm.avif](https://i.postimg.cc/ncHFK66x/temp-Imagee-Aq-GYm.avif)](https://postimg.cc/BtVf4wS7)

2. Setelah Optimisasi:
- Profiling
  [![temp-Image-Y6k-CAq.avif](https://i.postimg.cc/3xzQq6bd/temp-Image-Y6k-CAq.avif)](https://postimg.cc/jD61w8Tb)
- JMeter
  [![temp-Image-HTZg-Zn.avif](https://i.postimg.cc/prr0RVmx/temp-Image-HTZg-Zn.avif)](https://postimg.cc/n98K1JKw)

### Penjelasan pengurangan waktu eksekusi
- Terdapat pengurangan waktu eksekusi saat mengakses `/all-student` dari rata-rata 40241ms menjadi 1537ms di *Profiling Intellij*
- Terdapat pengurangan waktu eksekusi saat mengakses `/all-student-name` dari rata-rata 1218ms menjadi 249ms di *Profiling Intellij*
- Terdapat pengurangan waktu eksekusi saat mengakses `/highest-gpa` dari rata-rata 210ms menjadi 189ms di *Profiling Intellij*

Proses optimasi menghasilkan peningkatan yang lumayan signifikan dalam waktu eksekusi *endpoint* yang diuji. Baik untuk *Profiling Intellij* atau JMeter sudah menunjukkan pengurangan waktu eksekusi sehingga menghasilkan waktu respons yang lebih cepat untuk tiap *endpoint*.

### Pertanyaan refleksi
**1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?** <br>
Pendekatan pengujian kinerja dengan JMeter melibatkan simulasi tindakan pengguna untuk mengevaluasi respons aplikasi secara umum, seperti waktu respons dan throughput. Di sisi lain, IntelliJ Profiler memberikan analisis mendalam tentang bagian kode yang memakan waktu dan pola penggunaan sumber daya seperti memori dan CPU. Ini memungkinkan identifikasi dan optimalisasi pada area yang signifikan dalam kinerja aplikasi.

**2. How does the profiling process help you in identifying and understanding the weak points in your application?** <br>
Profiling dapat membantu kita memahami bagaimana kode bekerja dengan memonitor perilaku saat aplikasi berjalan, termasuk penggunaan CPU dan memori, serta aktivitas thread. Dengan menganalisis data ini, kita bisa menemukan ketidakoptimalan atau bottlenecks dalam aplikasi. Visualisasi dari alat profiling mempermudah identifikasi masalah dan memungkinkan optimisasi yang terarah.

**3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?** <br>
Ya, IntelliJ Profiler sangat efektif dalam membantu pengembang menganalisis dan mengidentifikasi masalah kinerja dalam kode aplikasi. Contohnya dalam modul 5 ini, kita dapat memperhatikan bahwa beberapa metode memiliki kinerja yang lebih lambat. Melalui kemampuannya untuk menampilkan durasi setiap baris kode, Profiler memungkinkan identifikasi mudah terhadap bagian program yang menjadi penyebab bottleneck.

**4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?** <br>
Tantangan utama dalam melakukan performance testing dan profiling adalah menginterpretasi output dan membandingkannya dengan hasil sebelumnya. Proses profiling menghasilkan banyak informasi yang memerlukan analisis teliti, sementara perlu juga menyimpan hasil sebelumnya untuk perbandingan. Untuk mengatasi tantangan ini, diperlukan kebiasaan dalam menggunakannya dan kehati-hatian dalam memperoleh data yang diinginkan.

**5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?** <br>
Menggunakan IntelliJ Profiler memungkinkan profil aplikasi terintegrasi langsung dengan IDE, menghilangkan kebutuhan untuk menggunakan third-party application. Ini mempermudah identifikasi bottlenecks dalam kode aplikasi.

**6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?** <br>
Ketika hasil dari profiling menggunakan IntelliJ Profiler tidak sepenuhnya konsisten dengan temuan dari pengujian kinerja menggunakan JMeter, langkah pertama adalah memeriksa kembali metode pengujian dan skenario yang digunakan. Penting juga untuk membandingkan metrik yang diukur untuk mengidentifikasi perbedaan fokus atau lingkup pengujian.

**7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?** <br>
Setelah menganalisis hasil pengujian kinerja dan profiling, strategi optimalisasi kode aplikasi dapat diterapkan. Langkah awal melibatkan pemeriksaan durasi program menggunakan JMeter untuk mengidentifikasi waktu eksekusi yang berlebihan. Kemudian, bagian kode yang bertanggung jawab dapat dioptimalkan. Penting untuk membandingkan output sebelum dan setelah modifikasi untuk memastikan fungsionalitas aplikasi tetap terjaga.