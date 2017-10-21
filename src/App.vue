<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view></router-view>
  </div>
</template>

<script lang="ts">

export default {
  name: 'app',

  mounted () {
    this.sum(1, 2, 3, '4', 5, null)
  },

  methods: {
    sum (...numbers: number[]): number {
      return numbers.reduce((r, c) => r + c, 0)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
