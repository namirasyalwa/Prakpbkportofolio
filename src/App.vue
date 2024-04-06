<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <div>
      <div class="cursor-1"></div>
      <div class="cursor-2"></div>
  
      <div id="menu-bars" @click="toggleMenu" :class="{ 'fa-times': menuActive }" class="fas fa-bars"></div>
  
      <header :class="{ active: menuActive }">
        <a href="#" class="logo"> <span>Namira</span> Syalwa </a>
        <nav class="navbar">
          <a href="#home">home</a>
          <a href="#about">about</a>
          <a href="#experience">experience</a>
          <a href="#contact">contact</a>
        </nav>
        <div class="follow">
          <a href="#" class="fab fa-github"></a>
          <a href="#" class="fab fa-instagram"></a>
          <a href="#" class="fab fa-linkedin"></a>
        </div>
      </header>
  
      <section class="home" id="home">
        <div class="content">
          <span class="hi"> hi there... </span>
          <h3> Saya <span> Namira Syalwa Alifa </span> </h3>
          <p class="info"> Seorang Software Engineer </p>
          <p class="text"> Seorang Mahasiswa Teknik Informatika Universitas Islam Riau yang Kreatif dan imajinatif!</p>
          <a href="#about"><Button @click="handleButtonClick">Tentang Saya</Button></a>
        </div>
        <div class="image">
            <svg class="home_blob" viewBox="0 0 200 187" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <mask id="mask0" mask-type="alpha">
                    <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547 
                    130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775 
                    97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666 
                    0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
                </mask>
                <g mask="url(#mask0)">
                    <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 
                    165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 
                    129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 
                    -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
                    <image class="home__blob-img" x="15" y="-25" href="./assets/images/profil1.png"/>
                </g>
            </svg>
        </div>
      </section>
  
      <!-- about section starts  -->
      <section class="about" id="about">
        <div class="center">
          <h1 class="heading"> about <span> me </span> </h1>
          <div class="row-1">
            <div class="image">
              <img src="./assets/images/profil2.jpeg" alt="profil image">
            </div>
            <div class="content">
              <h3> Saya Namira Syalwa Alifa dan Saya seorang Software Engineeer </h3>
              <p>Sebagai individu yang komunikatif, saya mampu beradaptasi dengan baik di berbagai situasi. Saya bisa bekerja efektif dalam tim maupun secara individu. Semangat saya dalam bekerja tinggi dan saya aktif dalam mempelajari hal-hal baru.</p>
              <div class="box-container">
                <div class="box">
                  <p> <span> Umur : </span> 19 </p>
                  <p> <span> Jenis Kelamin : </span> Perempuan </p>
                  <p> <span> Tempat Lahir : </span> Pekanbaru </p>
                  <p> <span> Tanggal Lahir : </span> 24 November 2004 </p>
                </div>
                <div class="box">
                  <p> <span> No. Telp : </span> +62 813-7019-8188 </p>
                  <p> <span> Email : </span> namirasyalwaa24@gmail.com </p>
                  <p> <span> Negara : </span> Indonesia </p>
                </div>
              </div>
              <a href="#" class="btn">download CV</a>
            </div>
          </div>
          <h1 class="heading"> <span> my </span> skills </h1>
          <div class="row-2">
            <div class="skills">
              <div class="progress">
                <h3> Web Development <span> 65% </span> </h3>
                <div class="bar"> <span></span> </div>
              </div>
              <div class="progress">
                <h3> Web Design <span> 80% </span> </h3>
                <div class="bar"> <span></span> </div>
              </div>
              <div class="progress">
                <h3> Microsoft Word <span> 90% </span> </h3>
                <div class="bar"> <span></span> </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- about section ends -->
  
      <!-- experience section starts  -->
      <section class="experience" id="experience">
        <div class="center">
          <h1 class="heading"> <span> my </span> experience </h1>
          <div class="box-container">
            <div class="box" v-for="(exp, index) in experiences" :key="index">
              <div class="content">
                <span>{{ exp.date }}</span>
                <h3>{{ exp.title }}</h3>
                <h4>{{ exp.position }}</h4>
                <p v-html="exp.description"></p>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- experience section ends -->
  
      <!-- contact section starts  -->
      <section class="contact" id="contact">
        <div class="center">
          <h1 class="heading"> contact <span> me </span> </h1>
          <div class="icons-container">
            <div class="icons">
              <i class="fas fa-envelope"></i>
              <h3>my email</h3>
              <p>namirasyalwaa24@gmail.com</p>
            </div>
            <div class="icons">
              <i class="fas fa-phone"></i>
              <h3>my number</h3>
              <p>+62 813-7019-8188</p>
            </div>
          </div>
          <div class="row">
            <form @submit.prevent="submitForm">
              <input type="text" placeholder="name" class="box" v-model="formData.name">
              <input type="email" placeholder="email" class="box" v-model="formData.email">
              <input type="number" placeholder="number" class="box" v-model="formData.number">
              <textarea placeholder="message" class="box" v-model="formData.message"></textarea>
              <input type="submit" class="btn" value="send message">
            </form>
          </div>
        </div>
      </section>
      <!-- contact section ends -->
  
      <!-- footer section starts  -->
      <footer class="footer">
        <p>&copy; 2024 Namira Syalwa. All rights reserved.</p>
      </footer>
      <!-- footer section ends -->
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  import Button from './components/button.vue'
  export default {
    components:{
      Button
    },
    mounted() {
    // Select cursor elements
    let cursor1 = document.querySelector('.cursor-1') as HTMLElement;
    let cursor2 = document.querySelector('.cursor-2') as HTMLElement;

    // Move cursors with mouse movement
    window.onmousemove = (e) => {
      cursor1.style.top = e.pageY + 'px';
      cursor1.style.left = e.pageX + 'px';
      cursor2.style.top = e.pageY + 'px';
      cursor2.style.left = e.pageX + 'px';
    };

    // Add cursor active class on link hover
    document.querySelectorAll('a').forEach(links => {
      links.onmouseenter = () => {
        cursor1.classList.add('active');
        cursor2.classList.add('active');
      };

      links.onmouseleave = () => {
        cursor1.classList.remove('active');
        cursor2.classList.remove('active');
      };
    });
  },
    data() {
      return {
        menuActive: false,
        formData: {
          name: '',
          email: '',
          number: '',
          message: ''
        },
        experiences: [
          {
            date: '2019 - 2021',
            title: 'Organisasi Passusbra SMA',
            position: 'Ketua Putri Angkatan',
            description: '•Bertanggung Jawab dengan Angkatan<br><br>•Mengkoordinasikan setiap kegiatan<br><br>•Mengkoordinasi Kelancaran Acara'
          },
          {
            date: 'November 2023',
            title: 'Informatic Futsal Cup IV Universitas Islam Riau',
            position: 'Panitia Acara',
            description: '•Membantu merancang susunan acara<br><br>•Admin informasi acara ke peserta<br><br>•Mengkoordinasi kelancaran acara'
          },
          {
            date: 'Desember 2023',
            title: 'Pra-Milad & Teknik Informatika ke-16',
            position: 'Sekretaris Pelaksana',
            description: '•Bertanggung jawab atas keberlangsungan acara<br><br>•Mengurus surat menyurat<br><br>•Membantu merancang susunan acara'
          },
          {
            date: 'Februari 2024',
            title: 'PEMILU 2024',
            position: 'Anggota KPPS',
            description: '•Menjadi Admin siRekap TPS<br><br>•Membantu menyiapkan segala perlengkapan PEMILU<br><br>•Mengkoordinasikan kelancaran acara'
          },
          {
            date: '2023-2024',
            title: 'Himatif Universitas Islam Riau',
            position: 'Sekretaris Dinas Kaderisasi',
            description:  '•Melaksanakan proker kaderasisi sekaligus menjadi sekretaris pelaksana kemah bakti mahasiswa angkatan 2023<br><br>'
          }
        ]
      };
    },
    methods: {
      handleButtonClick(){
        console.log('Button Clicked!')
      },
      toggleMenu() {
        this.menuActive = !this.menuActive;
      },
      submitForm() {
        // Handle form submission here
        console.log('Form submitted:', this.formData);
        // Reset form data after submission
        this.formData = {
          name: '',
          email: '',
          number: '',
          message: ''
        };
      }
    }
  };
  </script>

<style>
 @import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap');

 :root{
  --main-color:#de91ff;
}

*{
  font-family: 'Ubuntu', sans-serif;
  margin:0; padding:0;
  box-sizing: border-box;
  outline: none; border:none;
  text-decoration: none;
  text-transform: capitalize;
  transition: all .2s linear;
  line-height: 1.5;
}

html{
  font-size: 62.5%;
  overflow-x: hidden;
  scroll-behavior: smooth;
}

a{
  cursor: none;
}

body{
  background: #fcf2e8;
  padding-left: 30rem;
}

section{
    padding:2rem;
    margin: 0 auto;
    min-height: 100vh;
    max-width: 1200px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.heading{
    font-size: 4rem;
    padding-bottom: 1rem;
    color:#111;
    text-transform: uppercase;
}

.heading span{
    color:var(--main-color);
    text-transform: uppercase;
}

.btn{
    display: inline-block;
    margin-top: 1rem;
    padding:.8rem 3rem;
    background:var(--main-color);
    color:#fff;
    font-size: 1.7rem;
    border-radius: 2rem;
}

.btn:hover{
    background:#111;
    letter-spacing: .2rem;
}

header{
    position: fixed;
    top:0; left:0; bottom:0;
    background:#222;
    display: flex;
    align-items: center;
    justify-content: space-between;
    z-index: 1000;
    flex-flow: column;
    padding:8rem 2rem;
    width:30rem;
    text-align: center;
}

header .logo{
    text-transform: uppercase;
    color:#fff;
    font-size: 3rem;
    font-weight: bolder;
}

header .logo span{
    text-transform: uppercase;
    color:var(--main-color);
}

header .navbar a{
    display: block;
    font-size: 2rem;
    color:#fff;
    margin:2rem 0;
}

header .navbar a:hover{
    letter-spacing: .2rem;
    color:var(--main-color);
}

header .follow a{
    font-size: 2.5rem;
    color:#fff;
    margin:0 1rem;
}

header .follow a:hover{
    color:var(--main-color);
}

#menu-bars{
    position: fixed;
    top:2rem; right: 2rem;
    z-index: 10000;
    background:var(--main-color);
    color:#fff;
    border-radius: .5rem;
    padding:1rem 1.5rem;
    font-size: 3rem;
    display: none;
}

.cursor-1{
    position: absolute;
    top:0; left:0;
    height:1rem; width:1rem;
    background: var(--main-color);
    pointer-events: none;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    z-index: 10000;
}

.cursor-1.active{
    height:7rem;
    width:7rem;
    opacity: .3;
}

.cursor-2{
    position: absolute;
    top:0; left:0;
    height:4rem; width:4rem;
    border:.1rem solid var(--main-color);
    pointer-events: none;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    z-index: 10000;
    transition: .3s linear;
}

.cursor-2.active{
    display: none;
}

.home{
    flex-wrap: wrap;
    gap:1.5rem;
}

.home .image{
    flex:1 1 40rem;
}

.home__blob{
    width: 100%;
    fill: var(--main-color);
}

.home .image svg {
    width: 80%; /* Adjust the width as needed */
}

.home__blob-img{
    width: 160px;
}

.home .image img{
    width:100%;
}

.home .content{
    flex:1 1 40rem;
}

.home .content .hi{
    font-size: 2rem;
    color:var(--main-color);
}

.home .content h3{
    font-size: 4rem;
    color:#111;
    text-transform: uppercase;
}

.home .content h3 span{
    color:var(--main-color);
    text-transform: uppercase;
}

.home .content .info{
    font-size: 2.5rem;
    color:#111;
    padding:.5rem 0;
}

.home .content .text{
    font-size: 1.7rem;
    color:#666;
    padding:.5rem 0;
    line-height: 2;
}

.about .row-1{
    display: flex;
    flex-wrap: wrap;
    gap:2rem;
    padding-bottom: 2rem;
}

.about .row-1 .image{
    flex:1 1 25rem;
}

.about .row-1 .image img{
    height: 100%;
    width:100%;
    object-fit: cover;
    border:1rem solid #fff;
    border-radius: .5rem;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
}

.about .row-1 .content{
    flex:1 1 50rem;
}

.about .row-1 .content h3{
    color:#333;
    font-size: 3.5rem;
}

.about .row-1 .content p{
    color:#666;
    font-size: 1.7rem;
    padding:.5rem 0;
    line-height: 1.8;
}

.about .row-1 .content .box-container{
    display: flex;
    flex-wrap: wrap;
    gap:2rem;
    padding: 0.5rem 0;
}

.about .row-1 .content .box-container .box{
    flex:1 1 20rem;
}

.about .row-1 .content .box-container .box span{
    color:var(--main-color);
}

.about .row-2{
    display: block;
    flex-wrap: wrap;
    gap:2.5rem;
    align-items: center;
}

.about .row-2 .skills .progress {
  margin-bottom: 1rem;
}

.about .row-2 .skills .progress h3 {
  font-size: 1.7rem;
  color: #111;
}

.about .row-2 .skills .progress .bar {
  width: 100%;
  background: #ccc;
  height: 1rem;
  border-radius: 50rem;
}

.about .row-2 .skills .progress .bar span {
    display: block;
    height: 100%;
    background: var(--main-color);
    border-radius: 50rem;
  }
.about .row-2 .skills .progress:nth-child(1) .bar span {
  width: 65%;
}

.about .row-2 .skills .progress:nth-child(2) .bar span {
  width: 80%;
}

.about .row-2 .skills .progress:nth-child(3) .bar span {
  width: 90%;
}



.about .row-2 .box-container{
    flex:1 1 40rem;
    display: flex;
    flex-wrap: wrap;
    gap:1.5rem;
}

.about .row-2 .box-container .box{
    flex:1 1 20rem;
    background:#fff;
    padding:2rem;
    border-radius: .5rem;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
}

.about .row-2 .box-container .box h3{
    color:var(--main-color);
    font-size: 3rem;
}

.about .row-2 .box-container .box p{
    color:#666;
    font-size: 1.7rem;
    padding-top: .5rem;
}

.experience .box-container{
    display: flex;
    flex-wrap: wrap;
}

.experience .box-container .box{
    position: relative;
    flex:1 1 33rem;
    border-left: .2rem solid var(--main-color);
    padding-left: 2rem;
    padding-right: 2rem;
    padding-bottom: 2rem;    
}

.experience .box-container .box::before{
    content: '';
    position: absolute;
    top:0; left:-1rem;
    height:2rem;
    width:2rem;
    border-radius: 50%;
    background:var(--main-color);
}

.experience .box-container .box .content{
    background:#fff;
    padding:1.5rem;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
    border-radius: .5rem;
}

.experience .box-container .box .content span{
    color:#fff;
    font-size: 1.7rem;
    background:var(--main-color);
    border-radius: 50rem;
    padding:.4rem 1rem;
}

.experience .box-container .box .content h3{
    font-size: 2.5rem;
    padding:.5rem 0;
    color:#111;
}

.experience .box-container .box .content h4{
    font-size: 1.9rem;
}

.experience .box-container .box .content p{
    font-size: 1.7rem;
    color:#666;
    line-height: 1.8;
}


.contact .icons-container{
    display: flex;
    gap:1.5rem;
    flex-wrap: wrap;
    padding-bottom: 2rem;
}

.contact .icons-container .icons{
    flex:1 1 25rem;
    text-align: center;
    padding:3rem;
    background:#fff;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
    border-radius: .5rem;
}

.contact .icons-container .icons i{
    height:5rem;
    width:5rem;
    line-height: 5rem;
    font-size: 2rem;
    background: var(--main-color);
    color:#fff;
    border-radius: 50%;
}

.contact .icons-container .icons h3{
    color:#111;
    font-size: 2rem;
    padding:.5rem 0;
    padding-top: 1rem;
}

.contact .icons-container .icons p{
    color:#666;
    font-size: 1.7rem;
}

.contact .row{
    display: flex;
    flex-wrap: wrap;
    gap:1.5rem;
}

.contact .row form{
    flex:1 1 55rem;
    background:#fff;
    padding:0 2rem;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
    border-radius: .5rem;
}

.contact .row .map{
    flex:1 1 25rem;
    border:1rem solid #fff;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
    border-radius: .5rem;
    width: 100%;
}

.contact .row form .box,
.contact .row form textarea{
    width: 100%;
    border-bottom: .1rem solid #333;
    color:#333;
    text-transform: none;
    font-size: 1.7rem;
    padding:1rem 0;
    margin:1rem 0;
}

.contact .row form .box:focus,
.contact .row form textarea:focus{
    border-color: var(--main-color);
}

.contact .row form .box::placeholder,
.contact .row form textarea::placeholder{
    text-transform: capitalize;
}

.contact .row form textarea{
    height: 20rem;
    resize: none;
}

.contact .row form .btn{
    margin-top: 0;
    margin-bottom: 1.5rem;
}

.footer{
    margin-top: 2rem;
    font-size: 2rem;
    padding:2.5rem;
    text-align: center;
    color:#666;
    background: #fff;
}

.footer span{
    color:var(--main-color);
}


















/* media queries  */
@media (max-width:991px){

    html{
        font-size: 55%;
    }
    
    body{
        padding: 0;
    }

    #menu-bars{
        display: initial;
    }

    header{
        left:-120%;
    }

    header.active{
        left:0%;
    }

    .cursor-1,
    .cursor-2{
        display: none;
    }

}

@media (max-width:450px){

    html{
        font-size: 50%;
    }

    header{
        width:100%;
    }

    .experience .box-container .box{
        padding-right: 0;
    }

}
    </style>