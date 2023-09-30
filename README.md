# Improving Employee Retention by Predicting Employee Attrition Using Machine Learning
## Background
Sumber daya manusia (SDM) adalah aset utama yang perlu dikelola dengan baik oleh perusahaan agar tujuan bisnis dapat tercapai dengan efektif dan efisien. Pada kesempatan kali ini, kita akan menghadapi sebuah permasalahan tentang sumber daya manusia yang ada di perusahaan. Fokus kita adalah untuk mengetahui bagaimana cara menjaga karyawan agar tetap bertahan di perusahaan yang ada saat ini yang dapat mengakibatkan bengkaknya biaya untuk rekrutmen karyawan serta pelatihan untuk mereka yang baru masuk. Dengan mengetahui faktor utama yang menyebabkan karyawan tidak merasa, perusahaan dapat segera menanggulanginya dengan membuat program-program yang relevan dengan permasalahan karyawan.

## Objective
Membuat model pembelajaran mesin yang dapat memprediksi karyawan yang mengundurkan diri dan Memberikan rekomendasi bisnis berdasarkan model yang telah dibangun.

## Tools
Pada proyek ini saya menggunakan python sebagai bahasa pemrograman; Jupyter sebagai notebook; pandas, numpy, sklearn dan python ke bagian preprocessing dan machine learning; kombinasi matplotlib dan seaborn library untuk menghasilkan visualisasi data.

### Content
## Data Cleaning dan Data Preprocessing
Pada bagian ini terdapat beberapa proses seperti penanganan missing value. Nilai null pada feature Alasan Resign akan dimasukan dalam kategori masih_bekerja karena belum ada nilai pada feature Tanggal Resign yang berarti karyawan tersebut belum resign. Feature Ikut Program LOP akan di drop karena nilai nullnya sangat besar. Nilai null pada feature Jumlah Ketidakhadiran akan diisi dengan 0 dimana asumsi kita bahwa nilai null tersebut adalah karyawan belum pernah tidak hadir. Asumsi ini didukung dengan tidak adanya nilai 0 pada feature tersebut. Nilai null pada feature Skor Kepuasan Pegawai, Jumlah Keikutsertaan Projek dan Jumlah Keterlambatan Sebulan Terakhir akan diisi dengan nilai median dari masing-masing kolom.
Melakukan Feature Engineering  dan feature selection untuk melanjutkan ke dalam model. Melakukan feture encoding dengan label encoding dan One Hot Encoding. Melakukan split data feature dan target kemudian split data train 70%  dan test  30%.  Melakukan feature scaling dengan standarscaler. Karena terdapat data yang tidak seimbang maka akan ditangani dengan menggunakan SMOTE oversampling

## Annual Report on Employee Number Changes
![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/eb67ec02-37de-425a-a17f-933ef343a795)
**Observasi:**
Grafik tersebut menunjukkan pertumbuhan jumlah karyawan dari tahun ke tahun sejak 2006 - 2020. Dapat dilihat bahwa kondisi perusahaan sedang mengkhawatirkan karena jumlah karyawan yang terus berkurang selama 4 tahun terakhir. Ini bisa menjadi tanda bahwa perusahaan memiliki kemungkinan mengalami masalah baik internal maupun eksternal dari perusahaan.

## Resign Reason Analysis for Employee Attrition Management Strategy
![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/c65346cf-db63-41a5-beb9-a3f2fe6f84e7)

**Insight:**
Dari grafik diatas diketahui bahwa divisi Data Analyst merupakan divisi dengan persentase pengunduran diri tertinggi yaitu mencapai 50%

![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/4b0c9337-90d3-4c83-ad80-7cc0513eef3c)

**Insight:**
Pada grafik di samping di dapatkan bahwa semua karyawan yang berstatus resign pada divisi Data Analyst adalah dari Fresh Graduate Program dimana program tersebut juga memiliki jumlah karyawan resign yang jauh lebih banyak dibanding jumlah karyawan yang masih bekerja.

**Rekomendasi:**
Perusahaan dapat memberikan kesempatan pengembangan diri yang lebih baik seperti menyediakan training di setiap divisi khususnya kepada karyawan baru memberikan tawaran gaji dan benefit yang lebih kompetitif kepada karyawan khususnya program fresh graduate, serta menciptakan lingkungan kerja yang lebih suportif.

![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/641c3ccb-d250-473d-a206-f8d7756a3c43)

**Insight:**
Grafik di samping menunjukkan bahwa dari 8 karyawan dari divisi Data Analyst yang Resign, 4 diantaranya memiliki performa sangat bagus dan 1 karyawan memiliki perfoma bagus. Hal ini tentu sangat merugikan untuk perusahaan karena karyawan yang resign adalah karyawan dengan performa yang baik.

**Rekomendasi:**
Perusahaan dapat menawarkan gaji, benefit dan work-life balance yang lebih baik kepada karyawan dengan performa yang bagus. Selain itu, perusahaan diharapkan dapat menawarkan jenjang karir dan pengembangan diri yang baik kepada karyawan dengan performa bagus agar karyawan tersebut merasa dihargai dan merasa akan memiliki jenjang karir yang baik di perusahaan kita dengan harapan karyawan-karyawan yang bagus tersebut akan memilih untuk bertahan di perusahaan.

![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/2fcaef1a-45be-4137-b2d0-5e8ffafa2ff2)

**Insight:**
Grafik disamping menunjukkan bahwa dari sekian banyak alasan resign, 6  karyawan dari divisi Data Analyst resign dengan alasan toxic culture dan 2 lainnya resign dengan alasan internal conflict. Kedua alasan tersebut cukup menggambarkan bahwa adanya faktor yang kurang baik dari posisi internal Data Analyst pada perusahaan ini.

**Rekomendasi:**
Perusahaan harus dapat mengatasi konflik internal yang terjadi antar karyawan dengan memfasilitasi pertemuan antar karyawan atau mediator untuk menyelesaikan masalah. Selain itu, perusahaan harus mengevaluasi kembali budaya organisasi yang ada untuk mencari tahu apa yang "toxic" bagi karyawan dan memastikan budaya yang dimiliki adalah budaya yang positif dan memotivasi karyawan!

## Data Modeling
Melakukan data modeling dan beberapa tuning hyperparameter. Model yang dipilih merupakan model dengan algoritma Decision Tree karena memiliki performa yang baik dibandingkan model lainnya. Terlihat perbedaan AUC train dan test tidak jauh, sehingga model ini tidak overfitting atau underfitting sedangkan model lainnya masih overfitting. Selain itu, metrik evaluasi seperti accuracy, precision, recall, dan f1-score juga memiliki nilai yang lebih baik dibandingkan model lainnya.
![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/f861aa86-ceec-4d13-9cd4-95a8a6b029a5)

## Presenting Machine Learning Products to the Business Users
![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/2d971e2e-7205-4cbc-9f85-2bf7ab90aa7a)

- **Observasi:**
Feature Lama Bekerja merupakan feature paling penting dan sangat dominan dibanding feature lainnya dalam memprediksi kemungkinan resign dari suatu karyawan. Adapun data SHAP value menunjukkan bahwa semakin kecil lama bekerja dari suatu karyawan, maka semakin besar kemungkinan karyawan tersebut untuk resign.

![image](https://github.com/Sakinahnr11/Mini_Project_5/assets/134293722/63a595cd-e716-4014-8e82-7ea2b0c9894f)

- **Observasi :**
Terlihat dari grafik disamping menunjukkan bahwa terdapat turnover yang sangat tinggi pada pegawai yang bekerja 0-4 tahun dimana artinya pegawai baru cenderung resign dibanding pegawai lama.

## Rekomendasi Bisnis 
- Perusahaan dapat memfokuskan upaya pada perbaikan program onboarding untuk memastikan pegawai baru merasa diterima dan siap secara keterampilan untuk menghindari lingkungan kerja yang toksik dan mengurangi tingkat turnover yang tinggi pada pegawai baru. Sediakan mentorship yang membantu mereka beradaptasi dengan lingkungan perusahaan. Bangun budaya kerja yang kolaboratif dan berdayakan, serta prioritaskan keseimbangan kerja-hidup. Fasilitasi komunikasi terbuka, akui kontribusi pegawai secara teratur. Terakhir, tangani masalah dengan cepat dan adil untuk menciptakan lingkungan kerja yang sehat dan berkelanjutan.
