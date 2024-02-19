# Capstone-Modul-3
### **Saudi Arabia Used Cars**


### **Contents**

1. Business Problem Understanding
2. Data Understanding
3. Data Preprocessing
4. Modeling
5. Conclusion
6. Recommendation

****

by : Refno Devianto

### **1. Business Problem Understanding**
**Context**

Berdasarkan Analisis Pasar Mobil Bekas Arab Saudi yang didapat dari [Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/saudi-arabia-used-car-market#:~:text=Saudi%20Arabia%20Used%20Car%20Market%20Analysis,7.36%25%20over%20the%20forecast%20period). Pasar Mobil Bekas Arab Saudi memiliki nilai sebesar 4,91 miliar dolar AS pada tahun 2021 dan diperkirakan akan mencapai valuasi bersih sebesar 8,69 miliar dolar AS pada akhir tahun 2027, dengan pertumbuhan CAGR yang solid sebesar 7,36% selama periode perkiraan.

Meskipun Saudi adalah negara terbesar kelima di Asia dan salah satu negara kunci di Timur Tengah. Wilayah ini selalu mendukung adopsi mobil bekas / bekas karena meningkatnya permintaan untuk mobil mewah yang terjangkau di segmen mobil bekas. Konsumen di Arab Saudi lebih memilih mobil bekas daripada mobil baru karena mobil-mobil ini menawarkan Price yang lebih baik, pembiayaan yang mudah, dan dukungan perawatan purnajual. Para pemain termasuk anggota terorganisir dan tidak terorganisir yang menawarkan kendaraan menyediakan program keterlibatan konsumen dan menawarkan diskon yang kompetitif untuk mempromosikan penjualan mobil bekas di Arab Saudi. Mempertimbangkan faktor-faktor utama ini, permintaan mobil bekas di Arab Saudi diperkirakan akan tetap tinggi selama periode perkiraan.

Pasar mobil bekas adalah pasar yang tidak menentu. Pasar mobil bekas berfluktuasi berdasarkan sejumlah faktor, baik yang nyata (atau dalam beberapa kasus yang dibayangkan) seperti halnya pasar lainnya. Setelah pasar yang booming, tampaknya Price mobil bekas akan segera turun. Jadi, masalahnya adalah bagaimana cara mendapatkan Price terbaik untuk menjual atau membeli agar kita tidak salah mengambil keputusan. Berdasarkan hal tersebut, kita mungkin harus memprediksi Price mobil bekas pada dataset yang berisi fitur (variabel) di dalamnya.

**Problem Statement**

Permasalahan terbesar dari Pasar Mobil Bekas adalah bagaimana cara menjual mobil bekas di Arab Saudi sehingga mereka tidak menjualnya dengan Price yang terlalu tinggi atau terlalu rendah. Price yang terlalu tinggi akan membuat konsumen tidak tertarik untuk membeli mobil tersebut, sedangkan Price yang terlalu rendah akan membuat mereka merugi.

Marketplace pasti menginginkan keuntungan yang besar dengan menjual Price mobil bekas dengan Price yang tetap berdasarkan tipe, jarak tempuh, opsi, dll. Bagaimana cara membuat Price yang kompetitif adalah salah satu masalah untuk mendapatkan keuntungan besar pada bisnis mereka.
**Goals**

Berdasarkan permasalahan tersebut, marketplace tentu perlu memiliki toll/alat yang dapat memprediksi `Price` mobil bekas untuk menentukan Price terbaik dalam menjual mobil bekas. Hal ini akan menyulitkan para marketplace untuk mengambil keputusan sendiri karena banyaknya jenis, variasi mobil, tipe mobil, dan lain-lain. Dengan Prediksi ini, mungkin akan menjadi alat bantu bagi pemangku kepentingan / pasar untuk membuat keputusan.
**Analytic Approach**

Melalui permasalahan ini, kita akan menganalisa data untuk dapat menemukan pola-pola fitur yang ada yang membedakan satu mobil dengan mobil lainnya.

Selanjutnya, kita akan membuat model regresi untuk membantu marketplace sebagai alat untuk membuat keputusan yang lebih baik dan terbaik dalam memprediksi Price mobil bekas. Tentunya kami ingin membuat model yang baik untuk membantu marketplace dan memuaskan pelanggan untuk membeli di channel mereka.

**Metric Evaluation**

Evaluasi metrik yang akan digunakan adalah RMSE, MAE, dan MAPE, di mana RMSE adalah nilai rataan akar kuadrat dari error, MAE adalah rataan nilai absolut dari error, sedangkan MAPE adalah rataan persentase error yang dihasilkan oleh model regresi. Semakin kecil nilai RMSE, MAE, dan MAPE yang dihasilkan, berarti model semakin akurat dalam memprediksi Price Mobil Bekas sesuai dengan limitasi fitur yang digunakan. 


### **Conclusion**
Dalam proyek ini, kita telah membangun sebuah model untuk memprediksi harga mobil bekas dengan beberapa kriteria yang telah ditentukkan di atas, dimana model ini dapat menjadi informasi pendukung yang berguna dalam menentukan harga jual dan beli mobil bekas bagi perusahaan maupun individu yang melakukan transaksi.


- Model terbaik yang digunakan disini adalah XGBoost Regressor.
- Hasil dari model menunjukkan bahwa fitur-fitur yang paling signifikan pengaruhnya adalah Make, Year dan Engine Size. 
- Performa model regresi dievaluasi menggunakan metrik RMSE (Root Mean Square Error), MAE (Mean Absolute Error), MAPE (Mean Absolute Percentage Error) dan R-Squared . Setelah melalui proses hyperparameter tuning, model yang dihasilkan tergolong cukup baik dan linear (XGBoost) dimana menghasilkan nilai small error metric values,(RMSE, MAE, MAPE) dan nilai R2 hampir mendekati 1.
- Nilai RMSE memiliki makna bahwa ketika model digunakan untuk memprediksi harga mobil bekas, perkiraan harga rata-ratanya dapat memiliki selisih sekitar 34.743,5 Riyal (RMSE) atau 18.176 (MAE) dari harga actual. Sedangkan nilai MAPE yang dihasilkan 0.3 yang menunjukkan error absolut pada Price yang diprediksi oleh model. Semakin kecil nilai MAPE berarti nilai taksiran semakin mendekati nilai sebenarnya.
- Ketika Price more than 200000, distribusi plot mulai irregular. Kita dapat melihat bahwa kadang-kadang kita mempunyai harga yang diprediksi tinggi dan kadang-kadang rendah setelah 200000.

Model yang diperoleh masih memiliki potensi untuk ditingkatkan melalui proses-proses tertentu. Namun, untuk saat ini, kami berasumsi bahwa model sudah mencapai hasil yang diharapkan. Selain itu, dalam proses pembuatan model, diperlukan pengetahuan yang mendalam mengenai industri mobil untuk dapat mengembangkan pengembangan model yang lebih baik lagi.

### **Recommendation** 

Berikut ini adalah beberapa rekomendasi yang dapat dilakukan untuk meningkatkan performa model:

1. Menambahkan fitur yang mengkategorikan jenis mobil menjadi classic atau non-classic. Hal ini penting karena harga mobil bekas terhadap mileage dan tahun pembuatan dapat berbeda secara signifikan antara mobil-mobil classic dan mobil-mobil biasa. Dengan memasukkan fitur ini ke dalam model, kemungkinan besar akan meningkatkan akurasi prediksi harga mobil bekas.

2. Melakukan analisis terhadap nilai error tertinggi yang dihasilkan oleh model, dengan mengelompokkan error menjadi 3 kategori, yaitu overestimation (5%), underestimation (5%), dan mayoritas yang memiliki error mendekati nilai mean (90%). Setelah itu, dilakukan pemeriksaan hubungan antara error tersebut dengan setiap variabel independen. Dengan demikian, dapat dilakukan proses training ulang dan menghindari variabel yang menyebabkan error tinggi.

3. Jika tersedia tambahan data yang signifikan, dapat mencoba menggunakan model yang lebih kompleks seperti recursive neural networks (RNN). Namun, perlu diperhatikan bahwa jika jumlah data dan fitur masih sebatas dataset yang ada saat ini, kemungkinan peningkatan performa model secara signifikan dengan menggunakan model yang lebih kompleks tidak terlalu besar.
