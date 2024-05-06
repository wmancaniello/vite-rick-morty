<script>
import axios from "axios";

import AppHeader from "./components/AppHeader.vue";
import AppCards from "./components/AppCard.vue";
import CardsList from "./components/CardsList.vue";

export default {
  components: {
    AppHeader,
    AppCards,
    CardsList,
  },
  data() {
    return {
      cardsArray: [],
    };
  },
  created() {
    axios
      .get("https://rickandmortyapi.com/api/character", {
        params: {
          num: 20,
          offset: 0,
        },
      })
      .then((resp) => {
        this.cardsArray = resp.data.data;
      });
  },
};
</script>

<template>
  <AppHeader />
  <CardsList :cardsArray="cardsArray" />
</template>

<style lang="scss"></style>
