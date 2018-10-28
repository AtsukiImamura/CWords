<template>
    <v-card color="#fffafa" height="100%">
        <v-card-title primary-title class="text-md-left text-sm-left text-xs-left pa-2">
            <div class="sub_column_title">
                <h2>{{ column.title }}</h2>
            </div>
            <div class="column_article">
                {{ column.article.slice(0,145)+' ......' }}
            </div>
        </v-card-title>
    </v-card>
</template>

<script>

export default{
  name: 'ColumnArticle',
  props: {
    column: Object
  },
  data () {
    return {
    }
  }
}

</script>

<style scoped>
</style>
