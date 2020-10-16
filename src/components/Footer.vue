<template>
  <footer class="footer">
    <div class="flex between footer-txt">
      <p class="footer-logo">estra inc.</p>
      <nav class="footer-nav">
        <ul>
          <li><a href="#">home</a></li>
          <li><a href="#">about</a></li>
          <li><a href="#">service</a></li>
          <li><a href="#">works</a></li>
          <li><a href="#">price</a></li>
          <li><a href="#">contact</a></li>
        </ul>
      </nav>
    </div>
    <small class="copy-right">Copyright2019 estra inc. All Rights Reserved.</small>
  </footer>
</template>

<style scoped>
.footer {
  height: 90px;
  background-color: black;
  text-align: center;
  color: white;
}

.footer-logo {
  font-size: 18px;
  font-weight: bold;
  color: white;
  line-height: 70px;
  margin-left: 30px;
}

.footer-nav li {
  display: inline-block;
  margin-right: 30px;
  line-height: 70px;
}

.footer-nav a {
  text-decoration: none;
  color: white;
  font-size: 12px;
}

.footer-nav a:hover {
  color: #cccccc;
}

.copy-right {
  font-size: 12px;
}

@media screen and (max-width: 480px){
  .footer-nav{
    display: none;
  }

  .footer-txt{
    justify-content: center;
  }

  .footer-logo{
    margin: 0;
  }
}
</style>