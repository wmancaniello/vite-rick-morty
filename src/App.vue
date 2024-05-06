<script>
import axios from "axios";

import AppHeader from "./components/AppHeader.vue";
import CardsList from "./components/CardsList.vue";

export default {
  components: {
    AppHeader,

    CardsList,
  },
  data() {
    return {
      cardsArray: [],
    };
  },
  created() {
    axios.get("https://rickandmortyapi.com/api/character").then((resp) => {
      this.cardsArray = resp.data.results;
    });
  },
};
</script>

<template>
  <AppHeader />
  <CardsList :cardsArray="cardsArray" />
</template>

<style lang="scss"></style>
