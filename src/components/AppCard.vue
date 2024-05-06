<script>
export default {
  props: {
    cardObj: Object,
  },
};
</script>

<template>
  <div class="section mt-2">
    <img :src="cardObj.image" :alt="cardObj.name" />
    <div class="card-body text-center">
      <h5 class="card-title">{{ cardObj.name }}</h5>
      <p class="card-text">{{ cardObj.species }} - {{ cardObj.status }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section {
  img {
    border-radius: 50%;
  }
}
</style>
