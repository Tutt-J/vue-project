<script>
export default {
  name: "SideBar",
  data() {
    return { activeItem: 'home' }
  },
  methods: {
    isActive: function (menuItem) {
      return this.activeItem === menuItem
    },
    setActive: function (menuItem) {
      this.activeItem = menuItem
    }
  }
}

</script>
<template>
  <b-sidebar  visible id="sidebar-1" class="my-sidebar"  shadow>
    <div class="pl-0">
      <a href="" v-on:click="setActive('home')" :class="{ active: isActive('home') }"><i class="fas fa-home"></i></a>
      <a href="" v-on:click="setActive('tutorials')" :class="{ active: isActive('tutorials') }">
        <i class="fas fa-graduation-cap"></i>
        <p>Tutoriels</p>
      </a>
      <a href="" v-on:click="setActive('questions')" :class="{ active: isActive('questions') }"><i class="fas fa-question"></i>
        <p>Questions</p>
      </a>
      <a href="" v-on:click="setActive('book')" :class="{ active: isActive('book') }"><i class="fas fa-address-book"></i>
        <p>Annuaire</p>
      </a>
    </div>
  </b-sidebar>
</template>

<style lang="scss">
.my-sidebar.b-sidebar-outer, .my-sidebar .b-sidebar {
  position: absolute !important;
}
.my-sidebar{
  width:70px;
  .b-sidebar-header{
    display:none !important;
  }
  a{
    display: block;
    text-align: center;
    text-decoration: none;
    position: relative;
    padding-top: 8px;
    width: 70px;
    height: 56px;
    color:#1e0521;
    &.active{
      background-color:#fecc50;
    }
    &:hover{
      background-color:#fecc50;
      text-decoration: none;
      color:white;

    }
    i{
      font-size:22px;
    }
    p{
      margin: 4px;
      font-size: 75%;
    }
  }
  .close{
    display:none;
  }
}

</style>