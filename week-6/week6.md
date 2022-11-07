# **_Writing and Presentation Test Week 6_**

## React JS - Proptypes

Prop Types merupakan sebuah lib yang dapat membantu memeriksa data props yang dikirim agar sesuai dengan ekspektasi.Dengan berkembangnya aplikasi kita, kit dapat menemukan banyak kesalahan atau bugs dengan pengecekan tipe data. Untuk beberapa aplikasi, kita dapat menggunakan ekstensi JavaScript seperti Flow atau TypeScript untuk melakukan pengecekan tipe data di aplikasi secara menyeluruh.

```js
import React from "react";
import PropTypes from "prop-types";

const MyComponent = (props) => {
  return (
    <div>
      <h1>{props.title}</h1>
      <h2>{props.subtitle}</h2>
      <h3>{props.age}</h3>
    </div>
  );
};
```

## React Router

React Router merupakan standar library untuk routing pada React. Standar routing berfungsi untuk membuat suatu website menjadi dynamic.Pada React, Router membantu untuk mengarahka page satu ke page yg lainnya berdasarkan path url yg ditentukan.

### Cara Menggunakan React Router

- npm install react-router-dom@6

- Menambahkan import { BrowserRouter } from "react-router-dom";

- Tambahkan BrowserRouter Lalu bungkus `</APP>`

## React Redux

React Redux adalah sebuah library yang digunakan untuk mengelola state pada aplikasi React. React Redux menyediakan komponen `<Provider>` yang digunakan untuk menyediakan store pada aplikasi React. React Redux juga menyediakan komponen `<Connect>` yang digunakan untuk menghubungkan komponen React dengan store. React Redux juga menyediakan komponen `<Connect>` yang digunakan untuk menghubungkan komponen React dengan store.

### Cara Menginstall Redux

- npm install redux react-redux

- Buat Folder Redux Pada Folder src

- Buat Folder store pada folder redux

- Buat folder reducer pada folder redux

- Buat folder actions pada redux

Setup awal selesai.

- `store` adalah sebuah tempat untuk menyimpan state pada aplikasi React atau Juga bisa disebut gudangnya data.

- `reducer` adalah sebuah fungsi yang digunakan untuk mengubah state pada store.

- `action` adalah sebuah objek yang berisi type dan payload.

## Redux Thunk

Redux Thunk adalah middleware yang memungkinkan Anda memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi. Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.
