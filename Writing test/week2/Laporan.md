# Writing-Test-FrontEnd-Week2

## **React JS Lanjutan**

---

### **Hooks**

---

> Hooks merupakan sebuah fitur yang baru yang memudahkan functional component agar bisa menggunakan state dan lifecycle lainnya. Hooks yang sering digunakan adalah useState dan useEffect.

**_Cara Penggunaan useState_**

        // 1. Import useState dari react

              import { useState } from 'react';

              function App() {
              // 2. Menuliskan useState hooks
              const [nama, setNama] = useState("Pijin");

              // 3. Pemanggilan data
                return <h1>Assalamu'alaikum, nama saya {nama}</h1>;

                }

              // Output: Assalamu'alaikum, nama saya Pijin

**_useEffect_**

> useEffect merupakan hooks yang bisa digunakan untuk menggunakan lifecycle pada functional component dengan mudah. Lifecycle yang ada di dalam hooks hanya menggunakan useEffect yang menyatukan componentDidMount, componentDidUpdate, dan componentWillUnmount.

- Fase Mounting adalah fase ketika components dibuat atau pertama kali dirender ke DOM.
- Fase Updating adalah fase ketika sebuah component akan dirender ulang, biasanya ini terjadi ketika ada perubahan pada state atau props yang mengakibatkan perubahan DOM.
- Fase Unmounting adalah fase ketika component dihapus dari DOM.

**_Cara Penggunaan useEffect_**

      // 1. Import useEffect dari react
      import { useEffect } from 'react';

      // 2. Tuliskan penggunaan useEffect sebelum render
      ...
      useEffect(() => {
      console.log(" ");
      }, [ ])
      ...

> Kelebihan menggunakan hooks, yaitu :
>
> - Penulisan lebih singkat, clean dan mudah dimengerti
> - Direkomendasikan oleh team yang sudah mendevelopt React

### **PropTypes**

---

> PropTypes merupakan sebuah library untuk mengatur/meminimalisir data yang di terima ke suatu komponen dan memastikan type data yang masuk pada suatu komponen. Jika tidak sesuai, maka akan muncul pesan error.

**Install Proptypes**

      npm install prop-types

### **React Router 6**

---

> React Router merupakan standar routing yang digunakan sebagai library React JS untuk mengarahkan website dari page satu ke page lainnya, dimana page tersebut diarahkan dengan menggunakan URL

#### **Basic Instalation**

    npm install react-router-dom@6

#### **Pemanggilan React-router**

    import * as React from "react";
    import * as ReactDOM from "react-dom";
    import { BrowserRouter } from "react-router-dom";

    ReactDOM.render(
    <BrowserRouter>
      {/* The rest of your app goes here */}
    </BrowserRouter>,
    root
    );


      import { Link } from "react-router-dom";

      function Home() {
      return (
        <div>
          <h1>Home</h1>
          <nav>
            <Link to="/">Home</Link> |{" "}
            <Link to="about">About</Link>
          </nav>
        </div>
        );
        }

_Note :_

- > `<Link>` merupakan double tag yang bertujuan untuk mengarahkan suatu menu ke menu lain sifatnya seperti seperti tag `<a></a>`

- > _to_ merupakan atribut untuk mengarahkan ke suatu path / nilai untuk ke suatu page

- > _`"/"`_ artinya adalah mengarahkan ke page utama \_

### **State Management React Redux**

---

#### **Konfigurasi menggunakan State Management Redux**

1.  Create Project
2.  Install package / depedencies yang dibutuhkan

    ## Core

    - redux
    - react-redux
    - redux-devtools-extention

          command install :
          npm install redux react-redux redux-devtools-extention

    ## Additional

    - react-router-dom@6

           command install : npm install react-router-dom@6

3.  Membuat folder dengan **store** di dalam folder dibuat lagi 2 folder dan 1 file diantaranya :

    > Folder **actions**

    > Folder **reducers**

    > File `store.js`

4.  Menambahkan 1 file core dengan `index.js` di dalam folder **actions**

5.  Pada folder **actions** tambahkan action interface yang dibutuhkan

6.  Menambahkan 1 file dengan dengan `index.js` di dalam folder **reducers**, lalu import core method **combineReducers**

7.  Pada folder **reducers** tambahkan file reducer sesuai dengan kebutuhan

8.  Pada file `store.js` import core method **createStore**, kemudian memanggil folder reducers

9.  Pada file `index.js` yang terdapat di root project **src** import core method `Provider` dan import `store.js`

### **State Management-Async Action With Redux Thunk and Middleware**

> Redux-Thunk adalah sebuah middleware yang memungkinkan kita memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi

> Redux-Thunk solusi ketika kita menggunakan fetch data dari sebuah External API atau yang memiliki side effect (proses ashynchronous).
