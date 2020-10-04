<script>
export default {
  name: "NavBar",
}
</script>
<template>
  <b-navbar class="py-4" toggleable="lg" type="dark" variant="info">

    <b-navbar-brand href="#">Comment je fais quoi ?</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
<!--      <b-navbar-nav>-->
<!--        <b-nav-item href="#">Tutoriels</b-nav-item>-->
<!--      </b-navbar-nav>-->

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#"><i class="fas fa-user mr-2"></i>Mon compte</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<style lang="scss">
.navbar.navbar-dark{
  background-color: #508066 !important;
}

.navbar-brand{
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  font-family: 'Caveat', cursive;
  font-size:2.5rem !important;
}
</style>

