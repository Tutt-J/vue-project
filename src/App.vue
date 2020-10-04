<template>
  <div id="app">
    <header class="mb-5">
      <NavBar/>
    </header>
    <SideBar/>
    <b-container >
      <router-view/>
    </b-container>
    <footer class="fluid-container">
      <p class="text-center">Copyright &copy; 2018, ABC Marketing. All Rights Reserved.</p>
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
footer {
  color: white;
  background-color:#72423a;
  position: absolute;
  bottom: 0;
  width: 100%;
  margin-top: 50px;
}
</style>
<script>
import NavBar from "@/components/NavBar";
import SideBar from "@/components/SideBar";
export default {
  components: {SideBar, NavBar}
}
</script>