# **_Writing and Presentation Test Week 2_**

## Hari ke - 1 : Javascript Dasar Scope & Function

## Scope

> Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

#### Analogi :

Kita semua bisa melihat bintang-bintang dilangit karena bumi bersifat global.

Namun jika kamu tinggal di Bandung, kamu tidak akan bisa melihat monas yang berada di jakarta. Monas bersifat local yaitu hanya berada di Jakarta.

### Blocks

Blocks adalah code yang berada didalam curly braces {}. Conditional, function, dan looping menggunakan blocks.

### Global Scope

Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.

```js
let webDevelopment = "Skilvul";
function skilvul() {
  return webDevelopment;
}
console.log(webDevelopment); // Output: Skilvul
```

### Local Scope

Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.

```js
function greeting() {
  let MyName = "Naza";
  return myName; // Naza
}

console.log(greeting()); // Naza
greeting(myName); // Error
```

## Function

Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya.

#### Contoh Function

```js
function greeting() {
  return "Hello World";
}
```

- `function` adalah Function Keyword
- `greeting()` adalah Identifier
- `return 'Hello World' ` adalah Function Body

### Memanggil Function

```js
greeting();
console.log(greeting());
```

### Jenis-jenis Function

- Classic

```js
function myFunction(param) {}
```

- With Variabel

```js
let myFunction = function (param) {};
```

- Arrow Function

```js
let myFunction = (param) => {};
```

### Parameter dan Argumen

#### Parameter Function

- Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.

- Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.

```js
function tambah(a, b) {
  return a + b;
}
```

#### Argumen Function

- Argumen adalah nilai yang digunakan saat memanggil function.

- Jumlah argumen harus sama dengan jumlah parameternya.

- Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.

```js
function tambah(a, b) {
  return a + b;
}

console.log(tambah(1, 2)); //Output: 3
```

#### Default Parameters

- Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.

- Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen.

```js
function hai(nama = "siapa") {
  return "Hello" + nama;
}

console.log(hai("Naza")); // Hello Naza
console.log(hai()); // Hello siapa
```

#### Function Helper

- Bisa menggunakan function yang sudah dibuat pada function lain.

```js
function tambah(angka) {
  return angka * 5;
}
function kurang(nomer) {
  return tambah(nomer) - 4;
}

kurang(5); // 21
```

#### Arrow Function

Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)

```js
const greeting = () => {
  return "Hello World";
};

const kurang = (a, b) => {
  return a - b;
};
```

#### Short Syntax Function

- Zero Parameters

```js
const functionName = () => {};
```

- Zero One Parameters

```js
const functionName = (paramOne) => {};
```

- Zero Two Parameters

```js
const functionName = (paramOne, paramTwo) => {};
```

- Single-Line Block

```js
const sumNumbers = (number) => number + number;
```

- Multi-Line Block

```js
const sumNumbers = (number) => {
  const sum = number + number;
  return sum;
};
```

## Hari ke - 2 : JavaScript Dasar - Data Type Built-in - Prototype and Method

Semua bahasa pemrograman memiliki struktur data bawaan, tetapi ini sering berbeda dari satu bahasa ke bahasa lainnya.

### Dynamic and weak typing

JavaScript adalah bahasa dynamic dengan tipe dynamic . Variabel dalam JavaScript tidak secara langsung terkait dengan jenis nilai tertentu, dan variabel apa pun dapat diberi (dan ditetapkan ulang) nilai dari semua jenis:

- Dynamic

```js
let foo = 42; // foo is now a number
foo = "bar"; // foo is now a string
foo = true; // foo is now a boolean
```

- Weak

```js
const foo = 42; // foo is a number
const result = foo + "1"; // JavaScript coerces foo to a string, so it can be concatenated with the other operand
console.log(result); // 421
```

### Tipe Data Javascript

Tipe data didalam Javascript di bagi menjadi 2 macam, yaitu Primitif dan Non-Primitif.

#### Tipe Data Primitif

Tipe data primitif artinya tipe data yang hanya bisa menyimpan sebuah nilai.

- String
- Boolean
- Number
- Null

#### Non-Primitif

Non primitive artinya tipe data yang dapat menyimpan banyak data.

- Array
- Objek

#### String

String digunakan untuk mewakili dan memanipulasi urutan karakter. String berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks. Beberapa operasi yang paling sering digunakan pada string adalah memeriksa length, membangun dan menggabungkannya menggunakan operator string + dan += , memeriksa keberadaan atau lokasi substring dengan indexOf()metode, atau mengekstrak substring dengan substring()metode.

#### Properti String

- Length untuk menghitung panjang string tersebut.

```js
let hewan = "kelinci";
console.log(hewan.length);
```

- Prototype adalah untuk menambah metode kedalam objek.

```js
String.prototype.reverse = function(){
  let s = " "
  for (let i = String(this).length-1; i >= 0; i-- {
    s = s + String(this)[i]
  }
  return s
}
console.log("hallo".reverse()) //Output: 'ollah'
```

#### Metode

- `replace()`

  ```js
  const str = "aku sedang belajar ngoding";
  console.log(str.replace("aku", "naza")); // naza sedang belajar ngoding
  ```

- `toUpperCase()`

  ```js
  console.log(str.toUpperCase());
  ```

- `toLowerCase()`

  ```js
  console.log(hewan.toLowerCase());
  ```

- split()

  ```js
  const str = "naza sedang belajar ngoding";
  console.log(str.split()); // ["naza sedang belajar ngoding"]
  console.log(str.split(" ")); // ["naza", "sedang", "belajar", "ngoding"]
  console.log(str.split(" ", 2)); //  ["naza", "sedang"]
  ```

#### Number

Number adalah objek pembungkus primitif yang digunakan untuk mewakili dan memanipulasi angka seperti 37atau -9.25.

#### Metode

- `parseInt()` mem-parsing argumen string dan mengembalikan bilangan bulat dari radix atau basis yang ditentukan.

```js
function roughScale(x, base) {
  const parsed = Number.parseInt(x, base);
  if (Number.isNaN(parsed)) {
    return 0;
  }
  return parsed * 100;
}

console.log(roughScale(" 0xF", 16));
// expected output: 1500

console.log(roughScale("321", 2));
// expected output: 0
```

- `isNaN()` menentukan apakah nilai yang diteruskan adalah NaNdan tipenya adalah Number. Ini adalah versi yang lebih kuat dari yang asli, global isNaN().

```js
isNan(12345); //false (Angka)
isNan("hallo"); //true (Bukan Angka)
```

- `toFixed()` Digunakan untuk mengambil beberapa angka yang berada di belakang koma.

```js
let x = 4.234562;
pi.toFixed(); //Output: '4'
pi.toFixed(1); //Output: '4.2'
pi.toFixed(3); //Output: '4.234'
```

#### Objek

```js
let aku = {
  nama: "naza",
  pekerjaan: "mahasiswa",
};
```

#### Array

```js
let laptop = ["Asus", "Lenovo", "Axioo"];
```

#### Math

Math adalah objek bawaan yang memiliki properti dan metode untuk konstanta dan fungsi matematika. Ini bukan objek fungsi.

#### Properti

- `Math.PI` adalah rasio keliling lingkaran dengan diameternya, sekitar 3,14159.

```js
Math.pi; // Output: 3.1415
```

- `Math.sqrt2` adalah akar kuadrat dari 2, sekitar 1,414:

```js
Math.sqrt2; //Output: 1.4426 / akar 2
```

#### Metode

- `Math.abs()` mengembalikan nilai mutlak suatu bilangan.

```js
Math.abs(-2); //Output: 2 / Menjadi Positif
```

- `Math.cbrt()` mengembalikan akar pangkat tiga dari suatu bilangan.

```js
console.log(Math.cbrt(64)); // expected output: 4
```

- `Math.ceil()` digunakan untuk membulatkan angka desimal ke atas.

```js
let angka1 = 2.5;
let angka2 = 2.3;

console.log(Math.ceil(angka1)); // Output: 3
console.log(Math.ceil(angka2)); // Output: 3
```

- `Math.floor()` digunakan untuk membulatkan angka desimal ke bawah.

```js
let angka1 = 2.5;
let angka2 = 2.3;

console.log(Math.floor(angka1)); // Output: 2
console.log(Math.floor(angka2)); // Output: 2
```

- `Math.pow()` digunakan untuk per pangkatan.

```js
math.pow(4, 2); //output: 16
```

## Hari ke - 3 : Intro Javascript DOM

DOM merupakan kependekan dari Document Object Model, DOM ini yakni object model standar bagi XML dan HTML yang memiliki sifat platform independent. Saat membuka sebuah halaman web pada browser, maka file HTML dari web akan dimuat serta ditampilkan pada layar perangkat.

#### Element

```html
<body>
  <div id="text"
    <p></p>
  </div>
</body>
```

#### Node

Bagian-bagian terkecil yang berada di HTML. Seperti text.

### Traversing

`getElementsByTagName()` Merupakan metode yang dapat digunakan untuk menampilkan koleksi semua elemen dengan nama tag yang ditentukan.

```js
let byTag = document.getElementsByTagName("p");
console.log(byTag);
```

`getElementByID()` Merupakan metode untuk menampilkan elemen dengan nilai yang ditentukan. getElementByID akan menampilkan nilai null jika elemen itu tidak ada. getElementByID merupakan metode yang sering digunakan.

```js
let byId = document.getElementById("hero");
console.log(byId);
```

`getElementsByClassName()` Merupakan metode yang digunakan untuk menampilkan kumpulan elemen dengan nama class. getElementsByClassName akan menampilkan HTML Collection.

```js
let byClass = document.getElementByClassName("nav-link");
console.log(byClass);
```

`querySelector()` Mengambil elemen html setiap elemen html dengan selector tag , class , id dll,

```js
let heroSection = document.querySelector("#hero");
console.log(heroSection);
```

`parentElement()` Mengambil parent element berdasarkan childnya

```js
let selectItem = document.querySelector(".item");
console.log(selectItem.parentElement);
```

dan masih banyak lagi cara untuk traversing.

## Hari ke - 4 : Javascript DOM Manipulation

### Syntax Manipulasi Element

- `createElement()` : Fungsinya untuk membuat elemen baru.

```js
const paragrafSatu = document.createElement("p");
heading.textContent = "Halo Semua!";
document.getElementById("main").appendChild(p);
```

- `innerHTML` : Fungsinya untuk mendapatkan dan mengatur konten HTML dari suatu elemen.

```js
document.querySelector("#list").innerHTML = "<li>Ikan</li>";
```

- `innerText` : Fungsinya untuk mendapatkan dan mengatur konten HTML dari suatu elemen.

```js
document.getElementById("nama-saya").innerText = "Hai Namaku Naza";
```

- `textContent` : Fungsinya untuk mendapatkan dan atur konten teks dari sebuah node.

```js
document.getElementById("heading").textContent = "Skilvul";
```

- `append()` : Fungsinya untuk menyisipkan node setelah node child terakhir dari node parent.

```js
//deklarasi getElement
me.append("is Append");
```

- `appendChild()` : Fungsinya untuk menambahkan node ke daftar node child dari node parent yang ditentukan.

```js
const atas = document.createElement("h1");
atas.textContent = "HALO SEMUA~";
document.getElementById("website").appendChild(atas);
```

- `remove` : Fungsinya untuk menghapus sebuah elemen.

```js
let atas = document.getElementById("website");
atas.remove();
```

`setAttribute` : Fungsinya untuk menambahkan attribute.

```js
link.setAttribute("class", "website");
```

`style.Properti` : Fungsinya untuk memberikan style pada html.

```js
atas.style.color = "blue";
atas.style.border = "2px solid red";
```

`style.remove.property` : Fungsinya untuk menghapus properti style.

```js
atas.style.removeProperty("color");
```

dan masih banyak cara unutk memanipulasi element pada DOM.

## Hari ke - 5 : Javascript DOM Events & Forms

> Event adalah kejadian yang terjadi di halaman web. Kejadian yang dimaksud di sini seperti aktivitas yang dikerjakan pada halaman web.

### Cara Menambahkan Item Pada HTML

#### Didalam HTML Tag

```html
<body>
  <button id="btn" onclick="alert('Selamat Datang')">Klik</button>
</body>
```

#### AddEventListener() Pada file .js

```js
let button = document.getElementById("btn")
button.addEventListener("click", function() {
    alert("Nama Saya Naza")
``
```

#### Event Property pada file .js

```js
let button = document.getElementById("btn");

paragraf.onclick = function () {
  alert("Nama Saya Naza");
};
```

### Jenis-jenis Event

- Click
- Focus
- Submit
- Hover
- Scroll
- Change
