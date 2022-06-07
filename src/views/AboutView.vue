<template>
<v-container>
  <h1 class="mb-5">This is an about page</h1>
  <CardList :card-item="cardDatas" @push-data="getData"></CardList>
  
</v-container>
</template>
<script type="module">
import CardList from '../components/CardList.vue'
import { cardData } from '../db'
export default {
  data: () => ({
    cardDatas: cardData
  }),
  methods: {
    getData(text) {
      console.log('外層資料',text)
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