# **_Writing and Presentation Test Week 5_**

## React JS Basic

React Js adalah sebuah library javascript untuk membuat tampilan (user interface) pada website. React Js dibuat oleh tim engineer Facebook.

### Keuntungan React JS

React JS membuat aplikasi front-end lebih cepat walaupun harus menghandle berbagai data. React JS dapat digunakan pada aplikasi berskala kecil hingga besar dan kompleks.

Sebelum dapat membuat file react harus menginstall dulu Node JS.

Command membuat file react :

```
npx create-react-app nama-app
cd nama-app
npm start // npm : module package.
```

### Javascript Extension (JSX)

JSX adalah ekstensi react untuk javasript. JSX terlebih dahulu akan dicompile menjadi javascript sebelum ditampilkan pada browser. JSX digunakan untuk menulis HTML pada file ekstensi javascript.

## React JS with Vite JS

Vite JS merupakan framework untuk membuat file folder dari beberapa bahasa pemrograman.

Command membuat file react dengan Vite JS :

```
npm create vite@latest nama_aplikasi --template react
y
react
cd nama_aplikasi
npm install
npm run dev
```

## Props and State

Props digunakan untuk komunikasi antara parent dan child. Props merupakan parameter dari function component. Props merupakan singkatan dari properties dimana argument diteruskan dari suatu component react ke component react lain melalui attribute HTML

State merupakan data local (nilai dari state ditentukan sendiri oleh suatu component). State digunakan untuk menghandle data component yang terus berubah. Data state bersifat private yang hanya dapat diakses di dalam component dimana state itu dibuat

### React JS With Bootstrap

Kita dapat memakai bootstrap dengan menaruh link cdn didalam file index.html atau menginstall melalui terminal dengan syntax :

```
npm install bootstrap
```

- Lalu import file bootstrap ke dalam folder src/main.jsx atau src/index.js
- CSS: import "bootstrap/dist/css/bootstrap.min.css"
- JavaScript: import "bootstrap/dist/js/bootstrap.bundle.min"

## React JS Event

React dapat menghandle sebuah event yang memiliki perbedaan dengan handling event pada DOM element.

```js
const eventHandle = () => {
  setState("naza");
};
```

## React Form

- React JS menggunakan form agar user bisa berinteraksi dengan halaman web, seperti mengisi biodata, login, register, mencari data, dan lainnya

- React, `textarea` menggunakan atribut value. sebuah form yang menggunakan `textarea` dapat ditulis dengan cara yang sangat mirip dengan sebuah form yang menggunakan masukan satu baris.

## React Lifecycle Method

**Struktur lifecycle**

- Constructor: inisialisasi struktur data pada suatu component
- Function: fungsi yang dibutuhkan pada komponen
- Render: proses return atau mengembalikan component asli.

Ada 3 Fase yaitu : Mounting , Updating ,Unmounting

`Mounting` Fase ketika components di buat atau pertama kali di render ke DOM.

`Updating` Fase ketika sebuah component akan di render ulang.

`Unmounting` Fase ketika component dihapus dari DOM yang sebelumnya didefinisikan.

## Hooks React JS

Hooks digunakan untuk memudahkan penggunaan functional components agar bisa menggunakan state dan lifecycle lainnya.
