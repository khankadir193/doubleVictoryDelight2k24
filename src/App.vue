<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <!-- <DummyComp /> -->
  <HeaderComponent />
  <HowToPlay />
  <LeaderBoardComp />
  
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
// import DummyComp from './components/DummyComp.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import HowToPlay from './components/HowToPlayComp.vue';
import LeaderBoardComp from './components/LeaderBoardComp.vue';




export default {
  name: 'App',
  components: {
    // HelloWorld
    HeaderComponent,
    HowToPlay,
    LeaderBoardComp
  }
}
</script>

<style>
html,
body {
  /* background-image: url(http://localhost:8080/img/header.52ac4778.jpg); */
  background-image: url('./assets/images/doubleVictoryBg.png');
  margin: 0;
  /* background-color: #F13737 !important; */
  height: 100vh;
  width: 100%;
  position: absolute;
  background-repeat: no-repeat;
  background-size: cover;
}

#app {
  max-width: 100vw;
  overflow: hidden;
}

/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
