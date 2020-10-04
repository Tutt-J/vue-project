<template>
  <div id="app" class="app">
    <div class="row justify-content-around">
      <Card v-for="item in info" :key="item.name" :tutorial="item"/>
    </div>
    <Pagination class="mt-4"/>
  </div>
</template>

<script>
const axios = require('axios');
import Card from "@/components/Card";
import Pagination from "@/components/Pagination";
export default {
  components: {Pagination, Card},
  data () {
    return {
      info: null
    }
  },
  mounted () {
    axios
        .get('http://127.0.0.1:3000/api/tutorials')
        .then(response => (this.info = response.data))
  }
}
</script>