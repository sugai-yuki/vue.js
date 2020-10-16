<template>
  <header class="header">
    <div class="flex between">
      <p class="header-logo">estra inc.</p>
      <nav class="header-nav">
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
    <div class="hamburger" @click="hamburger()" :class="{'active':isClass}">
      <span class="hamburger-border"></span>
      <span class="hamburger-border"></span>
      <span class="hamburger-border"></span>
    </div>
    <nav class="menu-cont" :class="{'open':isClass}">
      <p class="menu-cont-ttl">estra inc.</p>
      <ul class="menu-cont-inner">
        <li><a href="#">home</a></li>
        <li><a href="#">about</a></li>
        <li><a href="#">service</a></li>
        <li><a href="#">works</a></li>
        <li><a href="#">price</a></li>
        <li><a href="#">contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data(){
    return{
      isClass: false
    };
  },
  methods: {
    hamburger(){
      this.isClass = !this.isClass;
    }
  }
};
</script>

<style scoped>
  .header{
  height: 70px;
  background-color: black;
}

.header-logo{
  font-size: 18px;
  font-weight: bold;
  color: white;
  line-height: 70px;
  margin-left: 30px;
}

.header-nav li{
  display: inline-block;
  margin-right: 30px;
  line-height: 70px;
}

.header-nav a{
  text-decoration: none;
  color: white;
  font-size: 12px;
}

.header-nav a:hover{
  color: #cccccc;
}

@media screen and (max-width: 480px){
  .hamburger{
    position: absolute;
    cursor: pointer;
    top: 35px;
    right: 20px;
    transform: translate(0, -50%);
    width: 40px;
    height: 40px;
  }

  .hamburger-border{
    position: absolute;
    left: 2.5px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: white;
    transition: 0.8s;
  }

  .hamburger-border:nth-of-type(1){
    top: 10px;
  }

  .hamburger-border:nth-of-type(2){
    top: 20px;
  }

  .hamburger-border:nth-of-type(3){
    top: 30px;
  }

  .header-nav{
    display: none;
  }

  .hamburger.active .hamburger-border:nth-of-type(1){
    top: 20px;
    transform: rotate(45deg);
  }

  .hamburger.active .hamburger-border:nth-of-type(2){
    opacity: 0;
  }

  .hamburger.active .hamburger-border:nth-of-type(3){
    top: 20px;
    transform: rotate(-45deg);
  }

  .menu-cont{
    width: calc(100% - 80px);
    height: 100%;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background-color: white;
    box-shadow: 80px 0 rgba(0, 0, 0, 0.3);
    transition: 0.2s;
    z-index: 999;
  }

  .menu-cont-ttl{
    margin: 40px 20px;
    font-size: 2.2rem;
    color: black;
    font-weight: bold;
  }

  .menu-cont a{
    color: black;
    margin: 15px;
    padding: 5px;
    text-decoration: none;
    display: block;
    border-bottom: solid 0.5px black;
  }

  .menu-cont.open{
    left: 0;
  }
}
</style>