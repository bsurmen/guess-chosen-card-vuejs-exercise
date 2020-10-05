<template>
  <div class="game-area">
    <h1 class="title">
      Where is <span>the cat<strong>?</strong></span>
    </h1>
    <h4 class="description">
      After you choose cat cards, click on the folded card.
    </h4>

    <div class="container">
      <app-card v-for="(card, index) in 5" :key="index"></app-card>
    </div>

    <div class="container"></div>
  </div>
</template>

<script>
import Card from "./Card";

export default {
  components: {
    appCard: Card,
  },
};
</script>

<style scoped>
.title {
  text-align: center;
  color: rosybrown;
}

.title span {
  color: mediumpurple;
}

.title strong {
  color: darkred;
}

.description {
  color: grey;
  text-align: center;
}

.container {
  margin-top: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
