<template>
<div>
    <v-btn color="blue" @click="addData">新增產品資料</v-btn>
    <v-card class="mb-5" v-for="item in product" :key="item.name">
        <v-card-title class="subheading font-weight-bold">
            {{ item.name }} - {{ text }}
        </v-card-title>

        <v-divider></v-divider>

        <v-list dense>
            <v-list-item>
                <v-list-item-content>分類:</v-list-item-content>
                <v-list-item-content class="align-end">
                    {{ item.category }}
                </v-list-item-content>
            </v-list-item>

            <v-list-item>
                <v-list-item-content>原價:</v-list-item-content>
                <v-list-item-content class="align-end">
                    {{ item.price }}
                </v-list-item-content>
            </v-list-item>

            <v-list-item>
                <v-list-item-content>特價:</v-list-item-content>
                <v-list-item-content class="align-end">
                    {{ item.salePrice }}
                </v-list-item-content>
                </v-list-item>
        </v-list>
    </v-card>
</div>
</template>
<script>
export default {
  data: () => ({
    text: 'card 內文字',
    innerData: []
  }),
  props: ['product'],
  methods: {
      changePrice() {
        this.text = '外層呼叫內層方法而修改'
      },
      addData () {
        console.log('已點擊')
        let obj = {}
        obj.name = '可樂'
        obj.category = '飲料'
        obj.price= 30
        obj.salePrice = 25
        this.innerData.unshift(obj)
        console.log(this.innerData)
    }
  },
  watch: {
      addData () {
          this.innerData = this.product
      }
  },
  mounted () {
    this.innerData = this.product
  }
}
</script>