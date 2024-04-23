#### Nama : Muh. Kemal Lathif Galih Putra
#### NPM : 2206081225
#### Kelas : ADPRO - A
#### ASDOS : REN

## TUTORIAL - 8

### Refleksi
1. Try to answer the following questions, and write the answer in the and new file readme.md in
you repository.

    #### a) Pengertian AMQP

    AMQP, atau Advanced Message Queuing Protocol, adalah sebuah protokol yang memungkinkan aplikasi untuk saling berkomunikasi dengan aplikasi sumber yang mengirimkan informasi atau data. Dalam konteks ini, data dikirimkan melalui middleware messaging, yang memungkinkan klien untuk mengambil data yang mereka perlukan dari middleware ini.

    Pada URL amqp://guest:guest@localhost:567, AMQP merupakan protokol yang digunakan untuk melakukan transaksi data.

    #### b) Penjelasan Komponen URL: guest:guest@localhost:5672

    - guest:guest adalah representasi dari username dan password yang digunakan untuk autentikasi oleh server.
    - localhost:5672: 
        - localhost merujuk pada hostname dari server, di mana hostnya adalah perangkat lokal.
        - 5672 adalah port yang digunakan untuk AMQP.

### MQProcessWithSleep
![alt text](image-1.png)

Dalam contoh tersebut, saya menemukan bahwa ___Subsriber___ mengalami keterlambatan dalam menerima atau memproses data dari jalur pesan dengan jeda 1 detik (1000 ms) untuk setiap prosesnya. Akibatnya, pesan yang di-queued pada jalur pesan akan meningkat seiring dengan penambahan jeda yang diberikan, karena penerbit mengirimkan lebih cepat daripada ___Subsriber___ yang menerima. Dalam kasus saya, jumlah pesan yang di-queued pada jalur pesan adalah 35 untuk 10 kali menjalankan Penerbit.