<template>
<v-row>
      <v-col cols="12">
          <v-btn @click="changeTxt">外層修改內層</v-btn>
          <v-btn color="orange" @click="addCard">外層新增內層卡片</v-btn>
          <v-btn block @click="emit">加+++</v-btn>
          <v-btn block @click="pushData">發送資料</v-btn>
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
      changeTxt() {
        this.$refs.myCard.changePrice()
      },
      addCard() {
        this.$refs.myCard.addData()
      }
    }
  }
</script>