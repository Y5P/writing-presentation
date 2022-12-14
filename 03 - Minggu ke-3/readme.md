# Array  
## 1. Apa itu Array?
Array merupakan tipe data terstruktur yang berguna untuk menyimpan sejumlah data yang bertipe sama. Bagian yang menyusun array disebut elemen array(isi), yang masing-masing elemen dapat diakses tersendiri melalui indeks array. Sebuah array biasa di tulis menggunakan Square Bracket[].
```js
//ini adalah square bracket
[]
```
## 2. Memanggil sebuah array  
Sebelum memanggil array kita harus mengetahui terlebih dahulu bagian-bagian array. Berikut adalah salah satunya :

* Index merupakan baris yang ada pada array.
* Array dihitung dari index 0  

Nah setelah tau istilah diatas maka kita akan mencoba memanggil data kucing di bawah.
```js
let hewan = ["Kura-kura", "Burung", "Kucing","Buaya"]
```  
Saat kita ingin memanggil sebuah data array maka kita akan memulai menghitungnya dari 0. Karena kita menghitung dari 0 maka data kucing terdapat di index ke 2 maka kita bisa memanggilnya dengan perintah berikut.
```js
console.log(hewan[2]) 
//output : Kucing
```   
## 3. Update Array  
Kita bisa mengubah nilai dari beberapa index yang terdapat pada array. Hal ini mempermudah kita untuk mengubah data yang salah pada array. untuk mengubahnya kita bisa memanggil variable dan index array tersebut lalu menerapkan nilainya. Contohnya seperti berikut.
```js
let hewan = ["Kura-kura", "Burung", "Kucing","Buaya"]

console.log(hewan[0])
//output : Kura-kura

hewan[0] = "Penyu"

console.log(hewan[0])
//output : "Penyu"
```   
## 4. Method array
Dalam penggunaan sebuah array kita dapat mengenal beberapa method yang sudah di sediakan untuk memudahkan dalam penggunaan sebuah array. Beberapa method pada array tersebut adalah sebagai berikut :  
* **.push()** merupakan method yang digunakan untuk menambah item pada bagian akhir
* **.pop()** merupakan method yang digunakan untuk menghapus item pada index terakhir.
* **.sort()** merupakan method yang digunakan untuk mengurutkan item array baik secara ascending maupun descending.
* **.shift()** merupakan method yang digunakan untuk menghapus index pertama pada array.
* **.unshift()** merupakan method yang digunakan untuk menambahkan item pada bagian awal/index pertama.

## 5. Looping
Dalam mengelola data pada array yang banyak maka kita membutuhkan sebuah cara yang tepat agar mempermudah kita untuk melakukan hal tersebut. Dengan begitu looping adalah salah satu solusinya. Adapun beberapa cara melakukan hal tersebut yaitu :
* 1. **.map()** untuk melakukan perulangan pada array dengan mengouputkan kondisi baru.
```js
let ganjil = [1,3,5]

let genap = ganjil.map(res =>{
    return res*2
})

console.log(genap)
//output : [2,6,10]
```

* 2. **.forEach()** untuk melakukan perulangan pada setiap element yang terdapat pada array

```js
let nama = ["Yogi","Jihad","Nyoman"]
nama.forEach(res=>{
    console.log(res);
})
//output : 
//Yogi
//Jihad 
//Nyoman
```
## 6. Array Multidimensi
Array multidimensi adalah sebuah variabel yang menyimpan sekumpulan data yang memiliki tipe sama dan elemen yang akan diakses melalui banyak indeks atau subskrip atau bisa juga di sebut array di dalam array.   
```js
let umur = [
    ["Yogi",21],
    ["Shofi",20],
    ["Nyoman",20]
]
console.log("Umur "+umur[0][0]+" adalah "+umur[0][1])
//Umur Yogi adalah 21
```
# Object
## Apa itu object?  
Object adalah sekumpulan list dari tipe data primitif (terkadang juga tipe data reference) yang menyimpan nilai dengan konsep berpasangan name-value. Tiap item (yang lebih dikenal dengan nama variabel) disebut dengan property, dan function disebut dengan method.
```js
let bunga = {} //object kosong

let hewan = {
    nama:"kucing",
    isCarnivora:true,
    jumlah:3
}
```
## 2. Memanggil object
untuk memanggil sebuah object kita bisa menggunakan beberapa cara yang biasa digunakan oleh programmer yaitu :
```js
let hewan = {
    nama:"kucing",
    isCarnivora:true,
    jumlah:3
}

//cara pertama
console.log(hewan.nama) //output : kucing

//cara kedua
console.log(hewan['jumlah']) //output : 3
```
## 3. Update Object
Untuk mengupdate object caranya hampir sama seperti mengupdate pada array yaitu memanggil variable lalu melanjutkan memanggil properti keynya. jika key tidak terdapat pada object sebelumnya maka sistem akan otomatis menambahkan key tersebut.
```js
let hewan = {
    nama:"kucing",
    isCarnivora:true,
    jumlah:3
}

hewan.nama = "harimau"
hewan.ukuran = "besar"

console.log(hewan)

/*
Output : 
{ nama: 'harimau', isCarnivora: true, jumlah: 3, ukuran: 'besar' }
*/
```
## 4. Menghapus properti pada object
Kita juga bisa menghapus properti pada object dengan memanfaatkan perintah delete.
```js
let hewan = {
    nama:"kucing",
    isCarnivora:true,
    jumlah:3
}

delete hewan.jumlah

console.log(hewan)
/*
Output : 
{nama:"kucing",isCarnivora:true}
*/
```
## 5. Object Method
Kita bisa menambahkan method pada properti object. Caranya yaitu kita memasukan sebuah function pada value propertinya. contohnya seperti berikut :
```js
const pintu = {
    keluar: function(){
        return "Tutup pintu"
    },
    masuk: function(){
        return "Buka pintu"
    }
}
console.log(pintu.masuk()) // Output : Buka pintu
```

## 6. Looping pada Object
Looping pada object digunakan untuk membantu kita agar bisa mengakses/menampilkan seluruh properti object didalamnya.
```js
for(let key in object){
    
}
```
## 7. Array of Object
Persis seperti namanya array of objet merupakan object yang berada didalam sebuah array. Jadi didalam sebuah array terdapat sebuah object yang dimana saat kita mengakses index tersebut akan memanggil sebuah object.
```js
let hewan = [
    {
        nama:"Ayam",
        kaki : 2
    },
    {
        nama:"kucing",
        kaki : 4
    }
]

hewan.forEach(res =>{
    console.log(res)
})
```

# Rekursif
## 1. Apa itu rekursif?
Fungsi rekursif merupakan sebuah fungsi yang memanggil dirinya sendiri, baik secara langsung maupun tidak langsung. Rekursif merupakan salah satu teknik penyelesaian masalah yang sangat berguna. Ketika menyelesaikan masalah secara rekursif, umumnya kita memecah-mecah masalah besar menjadi banyak masalah yang lebih kecil, dan menyelesaikan masalah kecil tersebut dengan fungsi rekursif.
```js
function rekursif(){
    rekursif()
}

//rekursif dengan kondisi
function rekursif(){
    if(kondisi){
        //berhenti memanggil
    }else{
        rekursif()
    }
}
```
## 2. Ciri-ciri rekursif
* Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
* Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.
## 3. Contoh kasus
```js
function pow(x,n){
    if (n==1){
        return x
    }else{
        return x * pow (x,n-1)
    }
}
console.log(pow(2,3)) // Output : 8
```

# Asynchronus
Asynchronus merupakan proses yang di lakukan secara bersamaan tanpa mengganggu aktivitas lainnya atau tidak berurutan. 

## Kunci utama pada Asynchronus
* **Callback** adalah sebuah fungsi yang di eksekusi di dalam fungsi lain yang memanggilnya.
```js
const notify = () => {

  console.log('Download complete!');

};

const download = (url, callback) => {

  console.log(`Downloading from ${url}....`);

  callback();

};

const url = 'https://brachio.site/download';

download(url, notify);
```
* **Promise** diilustrasikan seperti janji pada di dunia nyata. Promis memiliki 3 keadaan yaitu pending, rejected dan fuldilled.
```js
let progress = 100;

const download = new Promise((resolve, reject) => {

  if (progress === 100) {

    resolve('Download complete');

  } else {

    reject('Download failed');

  }

});
```
* **Async ??? await** adalah salah satu fitur baru dari javascript yang di gunakan untuk menangani hasil dari sebuah promise. Caranya adalah dengan menambahkan kata ???async??? di depan sebuah fungsi untuk mengubahnya menjadi asynchronous.Sedangkan await berfungsi untuk menunda sebuah kode di jalankan, sampai proses asynchronous berhasil.
```js
const getStatus = (url) => {

  console.log(`Downloading from ${url}...`);

  return new Promise((resolve, reject) => {

    setTimeout(() => {

      resolve('Download Complete');

    }, 3000);

  });

};

async function download(url) {

  let status = await getStatus(url); // tunggu sampai promise selesai

  console.log(status);

}

const url = 'https://brachio.site/download';

download(url);
```
# Storage
## 1. Local Storage
Local Storage merupakan salah satu cara yang dapat digunakan untuk menyimpan data di web browser. Pada localStorage penyimpanan data tidak memiliki kadaluarsa, artinya data yang disimpan tetap ada meskipun browser telah ditutup.  

Untuk menggunakan localstorage kita bisa menggunakan metode berikut:
1. setItem(key, value) digunakan untuk menyimpan data
2. getItem(key) digunakan untuk mengambil data
3. removeItem(key) digunakan untuk menghapus data berdasarkan key
4. clear() digunakan untuk menghapus semua data
5. key() digunakan untuk mengambil nomor dari setiap key   

```js
//menyimpan data
localStorage.setItem('key',value)

//mengambil data
localStorage.getItem('key')

//menghapus data
localStorage.removeItem('key')

localStorage.clear()
```

## Session Storage
Session Storage menyimpan data secara sementara, data akan menghilang saat tab ditutup atau browser ditutup. Metode dalam sessionStorage sama halnya dengan localStorage, untuk lebih mengetahui penggunaan mari kita coba

Untuk menggunakan localstorage kita bisa menggunakan metode berikut:
1. setItem(key, value) digunakan untuk menyimpan data
2. getItem(key) digunakan untuk mengambil data
3. removeItem(key) digunakan untuk menghapus data berdasarkan key
4. clear() digunakan untuk menghapus semua data
5. key() digunakan untuk mengambil nomor dari setiap key   
```js
//menyimpan data
sessionStorage.setItem('key',value)

//mengambil data
sessionStorage.getItem('key')

//menghapus data
sessionStorage.removeItem('key')

sessionStorage.clear()
```
