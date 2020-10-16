<template>
  <div id="app">
    <Header></Header>
    <main>
      <section class="eyecatch">
      <h1 class="eyecatch-txt">機械ではできない仕事を</h1>
      <div class="news flex">
        <div class="news-ttl">
          <p class="news-ttl-date">2019/01/01</p>
          <div class="news-ttl-cont">
            <a class="news-ttl-cont-txt">ニュースタイトルがここに入ります。３月の決算報告書</a>
          </div>
        </div>
        <button class="btn">news</button>
      </div>
    </section>
    <section class="mission">
      <img class="mission-img" src="./assets/mission-img.jpg">
      <div class="mission-txt">
        <h2 class="section-ttl">お客様のために進化する成長企業であり続ける</h2>
        <p class="mission-txt-cont">顧客主導型サービスを提供する企業として、お客様の会社経営に必要なサービスと情報を提供し続ける起業支援会社を目指します。企業が現在直面している「勝ち残るため」の戦略を提供できる会社として、ホームページをはじめ、各種マーケティングをご提供いたします。</p>
        <button class="btn">ミッション詳細</button>
      </div>
    </section>
    <section class="service">
      <h2 class="section-ttl">service</h2>
        <div v-for="(serv, index) in service" :key="index" :class="serv.num">
          <img class="service-img" :src="serv.img">
          <div class="service-txt">
            <h3>web制作事業</h3>
            <p class="service-txt-cont">コーチングのミッション</p>
            <p class="service-txt-cont">ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります</p>
            <button class="btn">サービス詳細</button>
          </div>
        </div>
    </section>
    <section class="info">
      <div class="info-conts flex between">
        <a class="company" href="#">
          <div class="center-txt">
            <h2 class="section-ttl">company</h2>
            <h3 class="sub-ttl">企業概要</h3>
          </div>
        </a>
        <a class="recruit" href="#">
          <div class="center-txt">
            <h2 class="section-ttl">recruit</h2>
            <h3 class="sub-ttl">採用情報</h3>
          </div>
        </a>
      </div>
      <a href="#" class="faq">
        <h2 class="section-ttl">FAQ</h2>
        <h3 class="sub-ttl">良くある質問</h3>
      </a>
    </section>
    <section class="contact">
      <div class="center-txt">
        <h2 class="section-ttl">contact</h2>
        <h3 class="sub-ttl">お問い合わせ</h3>
        <p class="b-txt">お気軽にお問い合わせください。</p>
        <p class="s-txt">資料請求・お問い合わせなどなんでも気軽にお問い合わせください。お仕事のご連絡もお問い合わせページに飛んでいただいて、入力フォームにご記入お願いいたします。</p>
        <button class="btn">お問い合わせへ</button>
      </div>
    </section>
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
  import Header from "./components/Header"
  import Footer from "./components/Footer"
  export default{
    data(){
      return{
        service: [
          {
            num: "service1",
            img: require("./assets/service2.jpg")
          },
          {
            num: "service2",
            img: require("./assets/service1.jpg")
          }
        ]
      };
    },
    components: {
      Header,
      Footer
    }
  };
</script>

<style>
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
    margin:0;
    padding:0;
    border:0;
    outline:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

body {
    line-height:1;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
    display:block;
}

nav ul {
    list-style:none;
}

blockquote, q {
    quotes:none;
}

blockquote:before, blockquote:after,
q:before, q:after {
    content:'';
    content:none;
}

a {
    margin:0;
    padding:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

/* change colours to suit your needs */
ins {
    background-color:#ff9;
    color:#000;
    text-decoration:none;
}

/* change colours to suit your needs */
mark {
    background-color:#ff9;
    color:#000;
    font-style:italic;
    font-weight:bold;
}

del {
    text-decoration: line-through;
}

abbr[title], dfn[title] {
    border-bottom:1px dotted;
    cursor:help;
}

table {
    border-collapse:collapse;
    border-spacing:0;
}

/* change border colour to suit your needs */
hr {
    display:block;
    height:1px;
    border:0;  
    border-top:1px solid #cccccc;
    margin:1em 0;
    padding:0;
}

input, select {
    vertical-align:middle;
}

/* 共通のスタイル */

.section-ttl {
  font-size: 24px;
}

.sub-ttl {
  font-size: 12px;
}

.flex {
  display: flex;
}

.around {
  justify-content: space-around;
}

.btn:focus {
  outline: none;
}

.btn:hover {
  cursor: pointer;
}

.between {
  justify-content: space-between;
}

/* 固有のスタイル */

.eyecatch {
  background: url(./assets/eyecatch.jpg) no-repeat;
  background-size: cover;
  background-position: center;
  height: 720px;
  position: relative;
}

.eyecatch-txt {
  font-size: 48px;
  font-weight: bold;
  font-style: italic;
  color: white;
  position: absolute;
  top: 60%;
  left: 10%;
  text-align: center;
}

.news {
  position: absolute;
  right: 0;
  bottom: 0;
  width: 50%;
  height: 50px;
}

.news-ttl {
  background-color: white;
  width: 80%;
}

.news-ttl-date {
  padding: 2px 0 8px 2px;
  font-size: 12px;
}

.news-ttl-cont{
  padding-left: 10px;
}

.news-ttl-cont-txt {
  color: black;
  text-decoration: none;
  font-size: 12px;
}

.news .btn {
  background-color: black;
  color: white;
  border: none;
  width: 20%;
}

.news-ttl-cont-txt:hover {
  cursor: pointer;
}

.mission {
  height: 400px;
  background-color: black;
  position: relative;
  margin-bottom: 150px;
}

.mission-txt {
  width: 50%;
  position: absolute;
  top: 50%;
  left: 20%;
  transform: translate(0, -50%);
}

.mission-txt .section-ttl {
  color: white;
  padding-bottom: 20px;
}

.mission-txt-cont {
  color: white;
  font-size: 12px;
  line-height: 1.5em;
  padding-bottom: 15px;
}

.mission-txt .btn {
  background-color: white;
  border: none;
  padding: 5px 15px;
}

.mission-img {
  height: 350px;
  position: absolute;
  bottom: -40px;
  right: 50px;
}

.service {
  background-color: #cecece;
}

.service .section-ttl {
  text-align: center;
  padding: 15px 0;
}

.service-img {
  width: 50%;
  position: absolute;
}

.service-txt {
  box-sizing: border-box;
  width: 40%;
  padding: 70px;
  background-color: white;
  font-size: 12px;
  position: absolute;
}

.service-txt-cont {
  padding-top: 10px;
  line-height: 1.5em;
}

.service-txt .btn {
  background-color: white;
  padding: 5px 15px;
  border: solid 1px black;
  display: block;
  margin: 10px 0 0 auto;
}

.service1 {
  position: relative;
  height: 700px;
}

.service2 {
  position: relative;
  height: 620px;
}

.service1 .service-img {
  top: 0;
  right: 0;
}

.service1 .service-txt {
  top: 100px;
  right: 40%;
}

.service2 .service-txt {
  top: 100px;
  left: 40%;
}

.info-conts {
  padding: 150px 0;
}

.company,
.recruit {
  display: block;
  background-size: cover;
  background-position: center;
  width: 48%;
  height: 250px;
  position: relative;
  color: white;
  text-decoration: none;
}

.company{
  background-image: url(./assets/company.jpeg);
}

.recruit {
  background-image: url(./assets/recruit.jpg);
}

.center-txt {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  width: 100%;
}

.center-txt .section-ttl {
  line-height: 1.5em;
}

.faq {
  background-color: black;
  width: 80%;
  box-sizing: border-box;
  margin: 0 auto 150px;
  padding: 30px;
  display: flex;
  color: white;
  text-decoration: none;
}

.faq .sub-ttl {
  line-height: 24px;
  flex-grow: 1;
  text-align: center;
}

.contact {
  background: url(./assets/contact-bg.jpg) no-repeat;
  background-size: cover;
  background-position: center;
  height: 500px;
  color: white;
  position: relative;
}

.contact .section-ttl {
  line-height: 1.5em;
}

.b-txt {
  font-size: 24px;
  padding: 20px 0;
}

.s-txt {
  font-size: 12px;
  padding-bottom: 20px;
}

.contact .btn {
  background-color: transparent;
  border: solid 1px white;
  color: white;
  padding: 5px 15px;
}

@media screen and (max-width: 480px){
  .eyecatch-txt{
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .news{
    width: 100%;
    min-height: 50px;
    height: auto;
  }

  .mission{
    margin-bottom: 30px;
  }

  .mission-txt .section-ttl{
    line-height: 1.5em;
  }

  .mission-img{
    height: 100px;
  }

  .service1,
  .service2{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    height: auto;
    padding-bottom: 60px;
  }

  .service-img{
    width: 90%;
    position: static;
  }

  .service-txt{
    width: 90%;
    position: static;
    padding: 10px;
  }

  .info-conts{
    flex-wrap: wrap;
    padding: 50px 0;

  }

  .company,
  .recruit{
    width: 100%;
  }

  .faq{
    width: 96%;
    margin: 0 auto 50px;
  }

  .contact .center-txt{
    width: 80%;
  }

  .s-txt{
    padding-bottom: 40px;
  }
}
</style>
