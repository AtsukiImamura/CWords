<template>
  <v-layout row  class="ml-0 mr-0">
    <v-flex xs12 sm12 md12 offset-sm3 class="ml-1 mr-1">
      <v-card>
        <v-toolbar :color=box.color>
          <v-toolbar-side-icon></v-toolbar-side-icon>
          <v-toolbar-title>{{ box.title }}</v-toolbar-title>
        </v-toolbar>

        <v-list two-line>
          <template v-for="(word, index) in box.words">
            <v-responsive :aspect-ratio="16/1">
              <v-list-tile
                :key="word.id"
                avatar
                @click=""
                class="mt-0 mb-0"
              >
              {{ word.word_title }}
              </v-list-tile>
            </v-responsive>
            <v-divider
              :key="index"
            ></v-divider>
          </template>
        </v-list>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>

export default{
  name: 'TopBox',
  props: {
    box: Object
  },
  data () {
    return {

    }
  }
}

</script>

<style scoped>

</style>
