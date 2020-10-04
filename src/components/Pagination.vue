<script>
export default {
  name: "Pagination",
  methods: {
    linkGen(pageNum) {
      return pageNum === 1 ? '?' : `?page=${pageNum}`
    }
  }
}
</script>
<template>
  <div class="overflow-auto">
    <b-pagination-nav :link-gen="linkGen" :number-of-pages="10" align="center" use-router></b-pagination-nav>
  </div>
</template>

<style lang="scss">
.btn-primary{
  background-color: #fecc50;
  border-color: #010b8b;
}
</style>

