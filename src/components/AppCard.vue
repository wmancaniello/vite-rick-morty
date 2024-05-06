<script>
export default {
  props: {
    cardObj: Object,
  },
  computed: {
    image() {
      return this.cardObj.card_images[0].image_url_small;
    },
    species() {
      return this.cardObj.species
        ? this.cardObj.species
        : "nessuna specie"
    },
  },
};
</script>

<template>
  <div class="card">
    <img :src="image" alt="">
    <h4>{{ cardObj.name }}</h4>
    <p>{{ species }} - {{ cardObj.status }}</p>
  </div>
</template>

<style lang="scss" scoped></style>
