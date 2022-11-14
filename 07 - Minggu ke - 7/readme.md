# MONGODB
MongoDB adalah salah satu jenis database NoSQL yang cukup populer digunakan dalam pengembangan website. Berbeda dengan database jenis SQL yang menyimpan data menggunakan relasi tabel, MongoDB menggunakan dokumen dengan format JSON. 

Hal inilah yang dianggap membuat pengelolaan data menggunakan MongoDB lebih baik. Alhasil, banyak perusahaan besar seperti Adobe, Google dan ebay yang menggunakannya. 
## Mongoose
Mongoose adalah sebuah Object Document Mapper (ODM). Ini berarti Mongoose mengizinkan Anda untuk mendefinisikan obyek dengan skema yang benar-benar diketik yang dipetakan ke sebuah dokumen MongoDB.

Mongoose menyediakan jumlah fungsionalitas yang luar biasa yang berkaitan dengan pembuatan dan pengerjaan skema. Mongoose saat ini memiliki delapan tipe skema dimana propertinya disimpan seperti saat berada di MongoDB. Diantaranya:

* String
* Number
* Date
* Buffer
* Boolean
* Mixed
* ObjectId
* Array

## install mongose
```nodejs
npm install --save mongoose;
```
menghubungkan mongoose
```javascript
var mongoose = require('mongoose');
 
mongoose.connect('mongodb://localhost/mongoose_basics', function (err) {
 
   if (err) throw err;
 
   console.log('Successfully connected');
 
});
```

mengidentifikasikan skema
```javascript
var userSchema = mongoose.Schema({
    name: {
      firstName: String,
    lastName: String
    },
    created: Date
});
```

membuat dan menyimpan model
```javascript
var Author = mongoose.model('Author', authorSchema);
```

# Docker
Docker adalah layanan yang menyediakan kemampuan untuk mengemas dan menjalankan sebuah aplikasi dalam sebuah lingkungan terisolasi yang disebut dengan container. Dengan adanya isolasi dan keamanan yang memadai memungkinkan kamu untuk menjalankan banyak container di waktu yang bersamaan pada host tertentu.

Docker ini diperkenalkan pada tahun 2013 oleh Solomon Hykes pada acara PyCon. Beberapa bulan setelahnya docker secara resmi diluncurkan, tepatnya pada tahun 2014. Semenjak itu docker menjadi sangat populer di kalangan developer luar negeri, tetapi belum terlalu populer di Indonesia. 

## fitur-fitur docker
Setelah mengetahui pengertiannya, sekarang kita masuk ke fitur-fitur dari docker yang dapat kamu gunakan sesuai dengan kebutuhanmu.

* Docker engine  
Yang pertama ada docker engine. Ia digunakan untuk membuat image dan container.

* Docker Hub  
Selanjutnya adalah docker hub. Ia adalah registry yang berisikan kumpulan dari image-image. Dengan menggunakan docker hub ini kamu dapat mengumpulkan image. Hub ini berbeda dengan docker engine yang hanya membuat image.

* Docker Compose  
Docker compose ini adalah salah satu fitur unggulan yang berfungsi untuk menjalankan beberapa container atau biasa disebut multi-container sehingga dapat menghemat banyak waktu.

* Docker for Mac  
Untuk fitur yang satu ini, kamu pasti sudah tau dari namanya. Fitur ini memungkinkan pengguna docker untuk menjalankan container pada sistem operasi Mac.

* Docker for Linux  
Sama seperti fitur sebelumnya, fitur ini juga memungkinkan penggunanya untuk menjalankan container pada sistem operasi Linux.

* Docker for Windows  
Fitur terakhir dan sudah pasti fitur yang paling banyak digunakan dibandingkan dengan fitur-fitur lainnya yaitu docker for windows. Fitur ini memungkinkan penggunanya untuk menjalankan container pada sistem operasi windows.