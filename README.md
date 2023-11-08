# Investigate-Business-Hotel-using-Data-Visualization

“Sangat penting bagi suatu perusahaan untuk selalu menganalisa performa bisnisnya. Pada kesempatan kali ini, saya akan lebih mendalami bisnis dalam bidang perhotelan. Fokus yang saya tuju adalah untuk mengetahui bagaimana perilaku pelanggan dalam melakukan pemesanan hotel, dan hubungannya terhadap tingkat pembatalan pemesanan hotel. Hasil dari insight yang ditemukan akan  sajikan dalam bentuk data visualisasi agar lebih mudah dipahami dan bersifat lebih persuasif. ”

## Data Preprocessing
-Handle Missing Value <br>
  Mengatasi data null pada kolom company, agent, children, city. Pada kolom company, agent dan children kita mengatasinya dengan mengubah mereka menjadi 0, karena kita tidak tahu kira-kira company yang mana nih yang sebenernya berada di kolom null tersebut nah daripada kita miss information lebih baik kita isi 0 dulu saja, apabila sudah ada berita update mengenai data null company tersebut baru bisa kita ganti menjadi nilai yang sebenernya, begitupun dengan agent dan children. Sebenernya sama untuk city, namun bedanya pada agent tipe datanya adalah text maka kita akan mengubah menjadi unknown. 
-Replace inappropriate values <br>
  Mengganti value yang tidak sesuai, pada kolom meal terdapat 4 varian yaitu 'Breakfast', 'Full Board', 'Dinner', 'No Meal', 'Undefined’, karena no meal dengan undefined sama aja. Maka kita akan mengubah undefined menjadi no meal
-Convert type data int to bool <br>
  Karena isi dari data is_repeated_guest yes or no, maka lebih baik diubah jadi bool
-Drop unnecessary data <br>
  Karena children, babies termasuk pengunjung, yang tidak ada bedanya (dari segi harga) maka akan dinamakan total_visitors
karena weekend dan weekdays sama aja untuk menghitung durasi pengunjung maka akan diganti menjadi stay_duration

    
## Monthly Hotel Booking Analysis Based on Hotel Type
  ![image](https://github.com/ariniamsr/Investigate_Hotel_Business/blob/main/1.png)
- Interpretation: <br>
Jumlah rata-rata pemesanan hotel tertinggi pada bulan Juli dan Resort Hotel dicapai pada bulan Juni Hal ini dikarenakan adanya libur Idul Fitri dan libur sekolah. Dan juga ada pertumbuhan rata-rata jumlah pemesanan hotel pada bulan Desember untuk City Hotel dan Resort Hotel, Hal ini dikarenakan libur Natal dan liburan malam tahun baru
![image](https://github.com/ariniamsr/Investigate_Hotel_Business/assets/117062760/5c50412d-cfe6-4184-bdd9-458b8a221b89)


## Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates

  ![image](https://github.com/ariniamsr/Investigate_Hotel_Business/blob/main/2.png)

- Interpretation: <br>
Semakin lama pelanggan menginap, semakin tinggi tingkat pembatalan pemesanan. Durasi menginap paling banyak dibatalkan (cancellation rate) untuk city hotel terjadi pada minggu ke 5 sedangkan pada resort hotel terjadi pada minggu ke 8. dapat dilihat dari grafik bahwa banyaknya seseorang membatalkan pemesanan dimiliki oleh resort hotel dibandingkan dengan city hotel, karena jika di city hotel seseorang kemungkinan tidak akan reservasi hotel lebih lama dibandingkan dengan resort hotel, karena Resort hotel sendiri ialah tempat yang digunakan untuk relaksasi, liburan dengan fasilitas yang lengkap. Beberapa kegiatan biasanya ditawarkan di resort, termasuk pijat, makanan, perawatan kosmetik, dan hiburan langsung. Bentuk bangunanya bisa seperti bangunan tunggal seperti hotel, lokasinya bisa berupa pulau tertentu atau seluruh pulau. Itu sebabnya resort hotel yang memiliki cancellation rate lebih tinggi dibandingkan dengan city hotel
![image](https://github.com/ariniamsr/Investigate_Hotel_Business/assets/117062760/e69b25fc-03c5-41d6-ac3e-ddbb3a3b678e)

  
## Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate

  ![image](https://github.com/ariniamsr/Investigate_Hotel_Business/blob/main/3.png)

- Interpretation: <br>
Lead time adalah masa tunggu atau jarak waktu pemesanan hotel hingga waktu kedatangan. Lead time di quarter pertama memiliki cancellation rate terendah dengan persentase 30.63 untuk city hotel dan 20.03 untuk resort hotel. Lalu untuk lead time tertinggi dimiliki pada quarter 4 dengan persentase 76.24 untuk city hotel dan 42.39 untuk resort hotel.
![image](https://github.com/ariniamsr/Investigate_Hotel_Business/assets/117062760/fd18c24c-ec49-4563-9f47-837b9db728e7)
