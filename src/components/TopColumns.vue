<template>
    <v-layout wrap justify-center id="top_columns">
        <v-flex d-flex xs12 sm12 md10 class="pa-0 mb-2">
            <v-card color="#ffffff" d-flex class="pa-0">
                <v-layout row wrap justify-center>
                    <v-flex child-flex xs12 sm7 md12 class="text-md-left ml-2 mr-2">
                        <v-toolbar color="white" flat>
                            <v-toolbar-title class="black--text">コラム</v-toolbar-title>
                        </v-toolbar>
                    </v-flex>
                </v-layout>
                <v-layout row wrap justify-center class="ml-2 mr-2">
                    <v-flex child-flex xs12 sm7 md7 class="pa-0">
                        <v-card color="#fffafa" height="100%" class="pa-0">
                            <v-card-title primary-title class="text-md-left text-sm-left text-xs-left pa-2">
                                <div class="column_title">
                                    <h2>{{ topColumn.title }}</h2>
                                </div>
                                <div class="column_article">
                                    {{ topColumn.article }}
                                </div>
                            </v-card-title>
                        </v-card>
                    </v-flex>
                    <v-flex d-flex xs0 sm5 md5 class="hidden-sm-and-down">
                        <v-layout row wrap>
                            <v-flex d-flex>
                                <v-layout row wrap>
                                <v-flex
                                    v-for="column in columns"
                                    :key="column.title"
                                    d-flex
                                    xs12
                                    class="pa-1"
                                >
                                    <ColumnArticle v-bind:column=column></ColumnArticle>
                                </v-flex>
                                </v-layout>
                            </v-flex>
                        </v-layout>
                    </v-flex>
                </v-layout>
                <v-layout row wrap justify-center>
                    <v-flex child-flex xs12 sm7 md12 class="text-md-left ml-2 mr-0">
                        <v-toolbar color="white" flat class="pa-0 ma-0">
                            <v-toolbar-title class="black--text"></v-toolbar-title>
                            <v-spacer></v-spacer>
                            <v-btn dark color="indigo" class="ma-0">
                                もっと読む
                                <v-icon right dark class="ma-0">forward</v-icon>
                            </v-btn>
                        </v-toolbar>
                    </v-flex>
                </v-layout>
            </v-card>
        </v-flex>
    </v-layout>
</template>

<script>
import TopColumnsStub from '../stub/columnsStub'
import ColumnArticle from '../components/ColumnArticle'

export default {
  name: 'TopColumns',
  components: {
    ColumnArticle
  },
  data () {
    return {
      lorem: 'Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.',
      topColumn: TopColumnsStub.data[0],
      columns: TopColumnsStub.data.slice(1)
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.hhf{
    height:100%;
}
.hhh{
    height: 50%;
}

.hhs{
    background-color: #ffffff;
}

.column_title{
    color: #101080;
    width: 100%;
    border-bottom: 2px solid #e0e0ff;
    margin-bottom: 2.5vh;
}
</style>
