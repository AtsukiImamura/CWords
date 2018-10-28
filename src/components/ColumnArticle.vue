<template>
    <v-card color="#fffafa" height="100%">
        <v-card-title primary-title class="text-md-left text-sm-left text-xs-left pa-2">
            <div class="sub_column_title">
                <h3>{{ column.title }}</h3>
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
.sub_column_title{
    color: #101080;
    width: 100%;
    border-bottom: 2px solid #e0e0ff;
    margin-bottom: 1.5vh;
    font-weight: 200;
}
</style>
