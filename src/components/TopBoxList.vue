<template>
    <v-layout row wrap justify-center class="mb-5">
        <v-flex d-flex xs12 sm4 md3 class="pl-1 pr-1">
            <v-card color="#3090a0"  class="pa-0" id="boxes_title_container">
                <v-toolbar color="white" flat class="pl-0">
                    <v-toolbar-title class="black--text">単語BOX</v-toolbar-title>
                </v-toolbar>
                <!--<div id="boxes_discription">-->
                <v-card-text id="boxes_discription">
                    <span class="article_span">
                        <span class="srg6">　単語BOX</span>
                        は、気になる単語をまとめて覚えるのに役立ちます。
                    </span class="article_span">
                    <span>
                    　まずは気になるBOXをのぞいてみましょう！ デフォルトのBOX以外にも他のユーザーがつくったBOXも検索してみましょう。
                    </span>
                    <span class="article_span">
                    　自分でBOXを作ることもできます。テーマを決め、それに合う単語を詰め込めば自分だけの単語BOXの出来上がりです！
                    </span>
                </v-card-text>
                <!--</div>-->
            </v-card>
        </v-flex>
        <v-flex d-flex xs12 sm8 md7 class="pa-0 pl-1 pr-1">
            <v-card color="#3090a0" d-flex class="pa-2">
                <v-layout row wrap justify-center>
                    <v-flex  xs12 sm5 md4  v-for="(box,index) in boxlist" v-bind:key=box.id class="ml-0 mr-0">
                        <TopBox v-bind:box=box v-if="index < maxBoxNum" class="ml-2 mr-2 mt-0 mb-0"></TopBox>
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
    },
    maxBoxNum: function () {
        //スクリーンサイズによって出すboxの数を変える
        switch(this.$vuetify.breakpoint.name){
            case 'xs':
                return 1;
            case 'sm':
                return 2
            default:
                return 3;
        }
    }
  }
}

</script>

<style scoped>
#boxes_title_container{
    height: 100%;
}
#boxes_discription{
    text-align: left;
    /*margin: 0px 3% 0px 5%;*/
    padding: 15px 3% 10px 5%;
    height: 80%;
    color: #ffffff;
}

.article_span{
    display: block;
    padding: 7px 0px 0px 0px;
}
</style>
