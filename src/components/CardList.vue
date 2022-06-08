<template>
<v-row>
      <v-col cols="12">
          <v-btn color="pink" @click="changePrice">生椰美式調漲+++</v-btn>
          <v-btn color="yellow" @click="changeTxt">外層修改內層內容</v-btn>
          <v-btn color="orange" @click="addCard">外層新增內層卡片</v-btn>
          <v-btn block @click="emit">About加+++</v-btn>
          <v-btn block @click="pushData">往About發送資料</v-btn>
          <!-- {{cardItem }} -->
          <v-divider  class="my-5"></v-divider>
          <card ref="myCard" :product="cardItem"></card>
      </v-col>
</v-row>
</template>
<script>
import card from '../components/Card.vue'
  export default {
    props: {
      'cardItem' :{
        type: Array,
        require: true
      }
    },
    components: {
      card
    },
    methods: {
      pushData() {
        this.$emit('push-data', 'CardList傳的資料')
      },
      emit() {
        this.$emit('add-num')
      },
      changePrice() {
        this.$refs.myCard.changePrice()
      },
      changeTxt() {
        this.$refs.myCard.changeText()
      },
      addCard() {
        this.$refs.myCard.addData()
      },
      addSecondCard() {
        // console.log('我是第二層')
        this.$refs.myCard.addData()
      }
    }
  }
</script>