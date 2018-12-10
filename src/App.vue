<template>
  <div id="app">
    <h1>I Pitty the Foo Bar</h1>
    <h3>{{ count }}</h3>
    <button v-on:click="incrementCount">+</button>
    <button v-on:click="decrementCount">-</button>

    <h1 v-if="isZero"></h1>
    <div v-else-if="isFooBar">
    <h1>You are FooBar</h1>
    <img src="./assets/mr-t.jpg" alt="Its Mr. T" />
    </div>
    <h1 v-else-if="isFoo">You are Foo</h1>
    <h1 v-else-if="isBar">You are Bar</h1>
    <h1 v-else>No Foos, and no Bars</h1>
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
    },
    decrementCount() {
      this.count--
    }
  },
  computed: {
    isFooBar() {
      return this.count % 3 === 0 && this.count % 5 === 0
    },
    isFoo() {
      return this.count % 3 === 0
    },
    isBar() {
      return this.count % 5 === 0
    },
    isZero() {
      return this.count === 0
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
  margin-top: 200px;
}
</style>
