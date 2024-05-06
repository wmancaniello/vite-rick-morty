<script>
import axios from "axios";

import AppHeader from "./components/AppHeader.vue";
import AppCards from "./components/AppCard.vue";
import CardsList from "./components/CardsList.vue"

export default {
  components: {
    AppHeader,
    AppCards,
    CardsList,
  },
  data() {
    return {};
  },
  created() {
    axios
      .get("https://rickandmortyapi.com/api/character", {
        params: {},
      })
      .then((resp) => {
        this.cardArray = resp.data.data;
      });
  },
};
</script>

<template>
  <AppHeader />
  <AppCards />
</template>

<style lang="scss"></style>
