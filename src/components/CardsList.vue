<script>
import AppCard from "./AppCard.vue";

export default {
  components: {
    AppCard,
  },
  props: {
    cardsArray: Array,
  },
};
</script>

<template>
  <div class="container">
    <h1 class="text-center">Rick and Morty App</h1>
    <div class="row row-cols-4">
      <div v-for="card in cardsArray" :key="card.id" class="col">
        <AppCard :cardObj="card" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
