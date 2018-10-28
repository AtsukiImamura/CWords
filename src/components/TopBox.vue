<template>
  <v-layout row  class="ml-0 mr-0">
    <v-flex xs12 sm12 md12 class="ml-1 mr-1">
      <v-card>
        <v-toolbar :color=box.color>
          <v-toolbar-side-icon></v-toolbar-side-icon>
          <v-toolbar-title class="ml-0">{{ box.title }}</v-toolbar-title>
        </v-toolbar>
        <v-list>
          <template v-for="(word, index) in box.words">
              <v-list-tile
                :key="word.id"
                @click=""
                class="mt-0 mb-0 word_container"
              >
                <v-list-tile-content>
                  <v-list-tile-title> {{ word.word_title }}</v-list-tile-title>
                  <v-list-tile-sub-title> {{ word.discription }}}</v-list-tile-sub-title>
                </v-list-tile-content>
              </v-list-tile>
            </v-list-tile>
            <v-divider
                v-if="index + 1 < box.words.length"
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
.word_container a{
  display: block;
  height: 20px;
}
</style>
