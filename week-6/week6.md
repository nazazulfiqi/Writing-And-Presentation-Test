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
