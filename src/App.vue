<template>
  <div id="app">
    <h1>Timur Bikbaev</h1>
    <h2>DevOps Engineer</h2>
    <img id="photo" alt="Tim logo" src="./assets/avatar.jpg">
    <contacts mail="t.bikbaev@gmail.com"/>
  </div>
</template>

<script>
import contacts from './components/contacts.vue'

export default {
  name: 'App',
  components: {
    contacts
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 10px;
}
img#photo {
  width: 100px;
  height: auto;
  position: absolute;
  top: 1%;
  right: 1%;
}
</style>
