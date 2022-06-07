<template>
<v-container>
  <h1 class="mb-5">This is an about page: {{ text }} / {{ num }} </h1>
  <CardList :card-item="cardDatas" @push-data="getData" @add-num="addNum"></CardList>
  
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
      console.log('外層資料',text)
      this.text = text
    },
    addNum() {
      this.num ++
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