<template>
<v-row>
      <v-col cols="12">
          <v-btn block @click="emit">加+++</v-btn>
          <v-btn block @click="pushData">發送資料</v-btn>
          <card :product="cardItem"></card>
      </v-col>
</v-row>
</template>
<script>
import card from '../components/Card.vue'
  export default {
    methods: {
      pushData() {
        this.$emit('push-data', 'CardList傳的資料')
      },
      emit() {
        this.$emit('add-num')
      }
    },
    props: ['cardItem'],
    components: {
      card
    }
  }
</script>