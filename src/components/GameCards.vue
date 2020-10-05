<template>
  <div class="game-area">
    <p>{{ selectedCard }}</p>
    <h1 class="title">
      Where is <span>the cat<strong>?</strong></span>
    </h1>
    <h4 class="description">
      After you choose cat cards, click on the folded card.
    </h4>

    <div class="container">
      <app-card
        :class="{ shadow : selectedCard == card.id }"
        @click.native="selectedCard = card.id"
        v-for="(card, index) in cards"
        :key="index"
        :card="card"
      ></app-card>
    </div>

    <div class="container">
      <app-default-card></app-default-card>
    </div>
  </div>
</template>

<script>
import Card from "./Card";
import DefaultCard from "./DefaultCard";

export default {
  components: {
    appCard: Card,
    appDefaultCard: DefaultCard,
  },
  data() {
    return {
      selectedCard: null,
      cards: [
        {
          id: 1,
          component: "app-cards",
          image: require("../assets/card-1.jpg"),
        },
        {
          id: 2,
          component: "app-cards",
          image: require("../assets/card-2.jpg"),
        },
        {
          id: 3,
          component: "app-cards",
          image: require("../assets/card-3.jpg"),
        },
        {
          id: 4,
          component: "app-cards",
          image: require("../assets/card-4.jpg"),
        },
        {
          id: 5,
          component: "app-cards",
          image: require("../assets/card-5.jpg"),
        },
      ],
    };
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

.shadow {
  box-shadow: 0px 5px 48px #30969f !important;
  transition: box-shadow 0.5s;
}
</style>
