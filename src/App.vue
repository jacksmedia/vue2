<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <GameBoard msg="Let's play memory game!"/>
  <HelloWorld />
</template>

<script>
import GameBoard from './components/GameBoard.vue'
import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  components: {
    GameBoard,
    HelloWorld
  },
}
</script>

<style>
#app {
  font-family: 'Limelight', cursive, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f0dfde;
  padding: 2rem;
  background: -webkit-linear-gradient(270deg, rgba(66,0,0,.8), rgba(66,0,0,0) 66.6%),
              -webkit-linear-gradient(0deg, rgba(0,66,0,.8), rgba(0,66,0,0) 66.6%),
              -webkit-linear-gradient(90deg, rgba(0,0,66,.8), rgba(0,0,66,0) 66.6%);
  background: linear-gradient(270deg, rgba(66,0,0,.8), rgba(66,0,0,0) 66.6%),
            linear-gradient(0deg, rgba(0,66,0,.8), rgba(0,66,0,0) 66.6%),
            linear-gradient(90deg, rgba(0,0,66,.8), rgba(0,0,66,0) 66.6%);
}
</style>
