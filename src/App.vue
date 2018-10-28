<template>
  <v-app class="ma-0 pt-0">
    <AppHeader/>
    <TopColumns/>
    <TopBoxList/>
  </v-app>
</template>

<script>
import AppHeader from './components/AppHeader'
import TopColumns from './components/TopColumns'
import TopBoxList from './components/TopBoxList'

export default {
  name: 'App',
  components: {
    AppHeader,
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
