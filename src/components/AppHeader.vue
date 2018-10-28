<template>
    <v-layout row wrap>
        <v-flex d-flex xs12 sm12 md12 class="pa-0 ma-0">
            <v-toolbar 
                fixed
                color="#003080"
                dark
                flat
                scroll-off-screen
                scroll-target="#top_columns"
                >
                <v-toolbar-title class="white--text">中国語WordBox</v-toolbar-title>
            </v-toolbar>
        </v-flex>
    </v-layout>
</template>

<script>

export default{
  name: 'AppHeader',
  data () {
    return {

    }
  }
}

</script>

<style scoped>

</style>
