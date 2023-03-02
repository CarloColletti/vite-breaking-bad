<script>
import { store } from "./data/store";
import axios from "axios";
import AppMain from "./components/AppMain.vue";
export default {
  components: { AppMain },
  data() {
    return {
      store,
    };
  },
  methods: {
    fetchCards() {
      axios.get(store.url).then((response) => {
        store.yugiCards = response.data.data;
      });
    },
  },
  created() {
    this.fetchCards();
  },
};
</script>

<template>
  <header>
    <h1>
      Yu-Gi-Oh Api
    </h1>
  </header>
  <AppMain />
</template>

<style>
  main {
  background-color: #d48f3a;
  }

</style>
