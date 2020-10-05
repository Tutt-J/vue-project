<template>
  <div id="app" class="app">
    <div class="row justify-content-around">
      <Card v-for="item in info" :key="item.name" :tutorial="item"/>
    </div>
    <Pagination class="mt-4"/>
  </div>
</template>

<script>
import Card from "@/components/Card";
import Pagination from "@/components/Pagination";
import TutorialService from '../services/tutorial.service'
export default {
  components: {Pagination, Card},
  data () {
    return {
      info: null
    }
  },
  mounted () {
    TutorialService.getPublicContent().then(response => (this.info = response.data))
  }
}
</script>