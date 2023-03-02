<script>
import { store } from "../data/store";
import AppCard from "./AppCard.vue";

export default {
  components: { AppCard },
  data() {
    return {
      store,
    };
  },
};
</script>


<template>
  <main class="py-5">
    <section>
      <div class="container">
        <div class="row row-cols-5 my-5">
          <AppCard
                v-for="card in store.yugiCards"
                :immagine="card.card_images[0].image_url_small"
                :titolo="card.name"
                :archetipo="card.archetype"
              >
          </AppCard>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
section .container {
  background-color: white;
  min-height: 80vh;
  }
</style>
