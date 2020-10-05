<template>
  <div class="container">
    <h1>Congratulations!!!</h1>
    <button @click="newGame">New Game</button>
  </div>
</template>

<script>
export default {
  methods: {
    newGame() {},
  },
};
</script>

<style scoped>
.container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.container h1 {
  text-align: center;
  font-size: 333%;
  color: darkgreen;
  opacity: 0.5;
}
.container button {
  width: 200px;
  background-color: #fff;
  color: darkred;
  border: 1px solid darkgreen;
  height: 50px;
  font-size: 15px;
  border-radius: 5px;
  outline: none;
  transition: all 0.5s;
}
.container button:hover {
  background-color: darkgreen;
  color: #fff;
  transition: all 0.5s;
  cursor: pointer;
}
</style>
