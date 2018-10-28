<template>
    <v-layout row wrap justify-center>
        <v-flex d-flex xs12 sm12 md10 class="pa-2">
            <v-card color="#ffffff" d-flex class="pa-2">
                <v-toolbar color="white" flat>
                    <v-toolbar-title class="black--text">単語BOX</v-toolbar-title>
                </v-toolbar>
                <v-layout row wrap justify-center>
                    <v-flex  xs12 sm5 md4  v-for="(box,index) in boxlist" v-bind:key=box.id class="ml-0 mr-0">
                        <TopBox v-bind:box=box v-if="!isMobile || index < 1" class="ml-2 mr-2 mt-0 mb-0"></TopBox>
                    </v-flex>
                </v-layout>
            </v-card>
        </v-flex>
    </v-layout>
</template>

<script>
import boxes from '../stub/boxesStub'
import TopBox from '../components/TopBox'

export default{
  name: 'TopBoxList',
  props: {

  },
  components: {
    TopBox
  },
  data () {
    return {
      boxlist: boxes.data
    }
  },
  computed: {
    isMobile: function () {
      const mobileBreakpoints = ['xs', 'sm']
      return mobileBreakpoints.some(e => {
        return this.$vuetify.breakpoint.name === e
      })
    }
  }
}

</script>

<style scoped>

</style>
