<template>
  <div id="app">
    <h1>{{message}}</h1>
  </div>
</template>

<script>

import axios from 'axios'

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      message: ''
    }
  },
  mounted() {
    axios.get('/api').then(res => this.message = res.data)
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
