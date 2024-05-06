<script>
import AppCard from "./AppCard.vue";

export default {
  components: {
    AppCard,
  },
  props: {
    cardsArray: Array,
  },
  data() {
    return {};
  },
};
</script>

<template>
  <div class="container">
    <div class="row row-cols-4">
      <div v-for="card in cardsArray" class="col">
        <AppCard :cardObj="card" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
