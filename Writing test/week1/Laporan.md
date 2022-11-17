# Writing-Test-FrontEnd-Week1

## **React JS Basic**
-------------------
### **Introduction to React JS**

> - React JS dibuat oleh Tim Engineer Facebook
> - React JS merupakan library single page aplication untuk mempermudah dalam membuat project react.
> - React JS membuat aplikasi fron-end menjadi lebih cepat walaupun harus menghandle berbagai data.
> - React JS is dapat menerapkan konsep Modular. React JS membagi satu tampilan pada website menjadi komponen-komponen kecil.
> - React JS dapat digunakan pada aplikasi berskala kecil hingga besar dan kompleks
> - Contoh aplikasi yang menggunakan React JS : Facebook, Pinterest, Netflix, Instagram, Twitter,  Uber, Airbnb, Slack.
> - Komunitas React JS di seluruh dunia sangat besar. Kebanyakan perusahaan teknologi sudah menggunakan React JS

### **Instalasi React JS**
> 1. Download Node JS version >= 12 (Terbaru)
    https://nodejs.org/en/download

> 2. Check Node dan NPM
        
            node --version
            npm --version

> 3. Install Create React App Library

            npm install -g create-react-app
 
 ### **Inisialisasi Proyek**

> 1. Buka Terminal atau Command Prompt (CMD) Lakukan perintah pada terminal yang telah dibuka :

        npx create-react-app [name-project]

Contoh :

        npx create-react-app example-project-1

*note: **create-react-app** ini merupakan library yang memudahkan programmer untuk membuat sebuah project react dan harus membuatnya harus terkoneksi ke internet *

>2. Install library react-router

        npm install react-router-dom@6

### **Menjalankan proyek**

>1. Buka folder proyek yang telah dibuat, kemudian jalankan Terminal / CMD pada folder tersebut. Kemudian lakukan perintah

        npm run start


*Note :*
- *File extension dari javascript pada react adalah **.jsx***


### **Component**
> Component adalah salah satu core dari React JS. Component membagi UI dalam satuan-satuan kecil. Artinya dalam 1 page ada beberapa component yang bisa kita buat.

> Component dibuat jika component tersebut bersifat reusable code.
Pada sebuah project, kita membuat component jika component tersebut akan dibutuhkan di page lain.

*Note : penggunaan nama function di React JS harus diawali Huruf Besar*

### **Functional Component & Class Component**
>React JS merupakan component Based yang dapat dibagi menjadi 2 bagian, yaitu class component dan functionanl component.


1. **Class Component**
> Contoh penulisan class component

        import React, {Component} from "react";

        class CourseCard extends Component {
                render() {
                        return (
                                <div>

                                </div>
                        )
                }
        }

        export default CourseCard;

2. **Functional Component**
> Penulisan functional component ada 2, yaitu function biasa dan arrow function

- Function biasa
        
        import React from 'react'

        function CourseCard() {
        return (
                <div>CourseCard</div>
                )
        };

        export default CourseCard;

- Arrow function

        import React from "react";

        const CourseCard = () => {
        return(
                <>
                <h2>My Courses</h2>
                </>
                )
        };

        export default CourseCard;

*Note : **
- *Dalam 1 file component hanya memiliki 1 **export default**. Jika memiliki lebih dari 1 fungsi dalam 1 file component kita bisa menggunakan **export** agar bisa di render*
- *Satu komponen hanya bisa me-render 1 element, jadi jika lebih dari satu element, harus dibungkus dengan **parent element** yaitu `<></>` atau `<div></div>`*

- *kebanyakan kasus dan dokumentasi resmi React JS merekomendasikan menggunakan function*

### **State & Props**
> State dan props berhubungan dengan statefull component dan stateless component.

- Stateless component berarti tidak memiliki state, hanya memiliki props
- Statefull berarti memiliki state dan bisa mengirim state tersebut ke component

=> Props
> Props digunakan agar component memiliki data yang dinamis yang dikirim dari component lain (bisa reusable)

=> State
- > State adalah data lokal
- > Data yang ada pada lokal komponen, ketika ada perubahan data, maka akan di render ulang
- > Data ini hanya tersedia untuk component tersebut dan tidak bisa di akses dari component lain 
- >State ini hanya berlaku untuk komponen nya sendiri

### **Stying CSS**

> Kalau di React JS untuk styling bisa menggunakan 3 cara, yaitu
- External CSS
- Internal CSS
- Inline Style


### **Lifecycle Method**
> Lifecycle dari komponen React ada 3 fase yaitu :

> - Component DidMount : proses ketika page pertama kali dibuka
> - Component DidUpdate : ketika update data
> - Component WillUnmount 

**Struktur data**
- Constructor : inisialisasi struktur data pada suatu komponen
- Function : fungsi yang dibutuhkan dalam komponen
- Render : proses untuk menampilkan pada browser
