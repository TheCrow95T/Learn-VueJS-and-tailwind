<template>
  <div id="body">
    <div id="top-img"></div>
    <div id="navbar">
      <div id="menu-bar">
        MENU BAR
        <i id="show" class="fa fa-bars" @click="showMenu()"></i>
        </div>
      <div id="nav">
        <div>
          <i id="hide" class="fa fa-times" @click="hideMenu()"></i>
          <router-link to="/">Home</router-link>|
          <router-link to="/about">About</router-link>|
          <router-link to="/covid">Covid Status</router-link>|
        </div>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'app',
    methods: {
      showMenu(){
        let nav = document.getElementById("nav")
        nav.style.right = "0";
      },
      hideMenu(){
        let nav = document.getElementById("nav")
        nav.style.right = "-150px";
      }
    }

  }
</script>

<style>
#body{
  background-image: url("assets/back.jpg");
  position: static;
}

#top-img {
  background-image: url("assets/background.jpg");
  background-size: contain, cover;
  min-height: 80px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#navbar {
  padding: 30px;
  background-color: rgb(191 219 254);
  font-size: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 0 20px;
}

#nav a.router-link-exact-active {
  color: #4236aa;
}

#hide {
  display: none;
}

#menu-bar {
  font-weight: bold;
  font-size: 24px;
  display: none;
}


@media (max-width: 700px){
  #navbar {
    padding: 15px;
    font-size: 15px;
  }

  #menu-bar {
    font-weight: bold;
    display: inline-block;
  }

  #nav {
    position: fixed;
    background: rgb(165 185 242);
    height: 100vh;
    width: 150px;
    top: 0;
    right: -150px;
    text-align: left;
    z-index: 2;
    transition: 0.75s;
    display: flex;
    flex-wrap: wrap;
  }

  #nav ul li {
    display: block;
  }

  #hide {
    display: block;
    color: black;
    margin: 10px;
    font-size: 22px;
    cursor: pointer;
  }

  #show {
    padding: 0px 10px;
    color: black;
    font-size: 22px;
  }

  #nav ul {
    padding: 30px;
  }
}

</style>
