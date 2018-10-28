<template>
  <v-app class="ma-0 pt-0">
    <AppHeader/>
    <TopColumns id="top_columns"/>
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
  color: #2c3e50;
  margin-top: 60px;
}
#top_columns{
  margin-top: 10vh;
}
</style>
