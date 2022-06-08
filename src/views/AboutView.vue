<template>
<v-container>
  <v-btn color="green" @click="addCardList">最外層新增卡片</v-btn>
  <v-btn color="purple" @click="addPrice">最外層生椰++</v-btn>
  <h1 class="mb-5">This is an about page: {{ text }} / {{ num }} </h1>
  <CardList ref="cardList" :card-item="cardDatas" @push-data="getData" @add-num="addNum"></CardList>
  
</v-container>
</template>
<script type="module">
import CardList from '../components/CardList.vue'
import { cardData } from '../db'
export default {
  data: () => ({
    cardDatas: cardData,
    text: '',
    num: 0
  }),
  methods: {
    getData(text) {
      this.text = text
    },
    addNum() {
      this.num ++
    },
    addCardList() {
      this.$refs.cardList.addSecondCard()
    },
    addPrice() {
      this.$refs.cardList.changePrice()
    }
  }, 
  mounted()  {
    console.log(this.cardDatas)
  },
  components: {
    CardList
  }
}
</script>