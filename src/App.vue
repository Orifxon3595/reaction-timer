<template>
  <h1>Arifun timer reaksiyasi</h1>
  <button @click="start" :disabled="isPlaying">Play</button>
  <!-- <Block  v-if="isPlaying" :delay="delay"/> -->
</template>  

<script>
import Block from './components/Block.vue'

export default {
  name: "App",
  components: {
    Block
  },
  data() {
    return{
      isPlaying: false,
      delay: null
    }
  },
  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000;
      this.isPlaying = true;
      console.log(this.delay);
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;
  margin-top: 60px;
}
</style>
