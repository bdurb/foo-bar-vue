<template>
  <div id="app">
    <h3>{{ count }}</h3>
    <button v-on:click="incrementCount">+</button>
    <button>-</button>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    incrementCount() {
      this.count++
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
