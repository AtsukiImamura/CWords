<template>
  <div id="app">
    <v-app>
      <TopColumns/>
      <TopBoxList/>
    </v-app>
  </div>
</template>

<script>
import TopColumns from './components/TopColumns'
import TopBoxList from './components/TopBoxList'

export default {
  name: 'App',
  components: {
    TopColumns,
    TopBoxList
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
