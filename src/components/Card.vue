<script>
export default {
  name: "Card",
  props: ['tutorial']
}
</script>
<template>
  <b-card
      :title="tutorial.title"
      img-src="https://picsum.photos/600/300/?image=25"
      img-alt="Image"
      img-top
      tag="article"
      class="mb-2 col-12 col-md-4"
  >
    <b-card-text>
      {{tutorial.description }}
    </b-card-text>

    <b-button href="#" variant="primary">Accéder</b-button>
  </b-card>
</template>

<style lang="scss">
.btn-primary{
  background-color: #fecc50;
  border-color: #010b8b;
}
.card{
  border:none;
}
</style>

