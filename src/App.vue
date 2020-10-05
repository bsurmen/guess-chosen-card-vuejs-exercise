<template>
  <component :is="activeComponent"></component>
</template>

<script>
import Failure from "./components/Failure";
import GameCards from "./components/GameCards";
import Celebrate from "./components/Celebrate";

export default {
  data() {
    return {
      activeComponent: "app-game-cards",
    };
  },
  components: {
    appGameCards: GameCards,
    appCelebrate: Celebrate,
    appFailure: Failure,
  },
};
</script>

<style>
body {
  font-family: sans-serif;
}
</style>
