<template>
  <transition name="slideContainer" mode="out-in">
    <component
      :is="activeComponent"
      @activeComponentEvent="activeComponent = $event"
    ></component>
  </transition>
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

.slideContainer-enter-active {
  animation: slide-in 0.3s ease-in-out forwards;
}
.slideContainer-leave-active {
  animation: slide-out 0.3s ease-in-out forwards;
}

@keyframes slide-in {
  from {
    transform: translateX(-1000px);

    opacity: 0;
  }
  to {
    transform: translateX(0px);
    opacity: 1;
  }
}
@keyframes slide-out {
  from {
    transform: translateX(0px);
    opacity: 1;
  }
  to {
    transform: translateX(1000px);
    opacity: 0;
  }
}
</style>
