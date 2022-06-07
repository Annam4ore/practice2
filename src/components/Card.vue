<template>
<div>
    <v-card class="mb-5" v-for="item in product" :key="item.name">
        <v-card-title class="subheading font-weight-bold">
            {{ item.name }}
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
  props: ['product']
}
</script>