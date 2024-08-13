<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <tweet-toggle></tweet-toggle>
  </div>
</template>

<script>
import TweetToggle from './components/TweetToggle.vue'

export default {
  name: 'App',
  components: {
    TweetToggle
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
