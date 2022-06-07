<template>
<div class="about">
<h1>This is a settings page</h1>
<v-container>
     <v-card flat class="card_item" v-for="item in products" :key="item.name">
        <v-list subheader two-line color="#F5F5F5">
            <v-list-item>
                <v-list-item-content>
                    <v-list-item-title class="subtitle-2">產品名稱</v-list-item-title>
                    <v-list-item-subtitle class="mt-2">{{ item.name }}</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-content>
                   <v-list-item-title class="subtitle-2">分類</v-list-item-title>
                    <v-list-item-subtitle class="mt-2">{{ item.category }}</v-list-item-subtitle>
                </v-list-item-content>
               <v-list-item-content>
                   <v-list-item-title class="subtitle-2">原價</v-list-item-title>
                    <v-list-item-subtitle class="mt-2">NT$ {{ item.price }}</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-content>
                   <v-list-item-title class="subtitle-2">售價</v-list-item-title>
                    <v-list-item-subtitle class="mt-2">NT$ {{ item.salePrice }}</v-list-item-subtitle>
                </v-list-item-content>
            </v-list-item>
        </v-list>
        <v-divider color="#3f495e" class="divider_tab"></v-divider>
    </v-card>
</v-container>

<!-- <v-data-table
    :headers="headers"
    :items="products"
    :items-per-page="5"
    class="elevation-1"
  ></v-data-table> -->
</div>
</template>
<script>
  export default {
    data () {
      return {
        // headers: [
        //   {
        //     text: '產品名稱',
        //     align: 'start',
        //     sortable: false,
        //     value: 'name',
        //   },
        //   { text: '分類', value: 'category' },
        //   { text: '原價', value: 'price' },
        //   { text: '特價', value: 'salePrice' }
        // ],
        products: [
          {
            name: '生椰美式',
            category: '咖啡',
            price: 60,
            salePrice: 45
          },
          {
            name: '珍珠奶茶',
            category: '茶類',
            price: 70,
            salePrice: 55
          },
          {
            name: '西瓜汁',
            category: '果汁',
            price: 50,
            salePrice: 40
          },
          {
            name: '珍珠鮮奶',
            category: '鮮奶',
            price: 80,
            salePrice: 60
          },
          {
            name: '蘋果汁',
            category: '果汁',
            price: 60,
            salePrice: 50
          }
        ],
      }
    },
  }
</script>
