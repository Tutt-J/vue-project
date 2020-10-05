<template>
  <div id="app">
    <header class="fixed-top">
      <NavBar/>
    </header>
    <SideBar/>
    <img
        src="img/books.jpg"
        class="lazy" alt="">
    <b-container id="main-container" class="mb-5">
      <router-view/>
    </b-container>
    <footer class="fixed-bottom fluid-container py-2">
      <p class="text-center mb-0">Copyright &copy; 2020, Digistos. Tous droits réservés.</p>
    </footer>
  </div>
</template>

<style lang="scss">
@import './assets/scss/global.scss';
body {
  min-height: 100vh;
  position: relative;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
#main-container{
  margin-top:-100px;
}
footer {
  color: white;
  background-color:#72423a;
  width: 100%;
  margin-top: 50px;
}

img{
  height:350px;
  width:100%;
  object-fit:cover;
}

.card{
  background-color:transparent !important;
}

.card-img, .card-img-top{
  border-radius:0 !important;
}
</style>
<script>
import NavBar from "@/components/NavBar";
import SideBar from "@/components/SideBar";
export default {
  components: {SideBar, NavBar}
}
</script>