<template>
  <v-app>
    <TopToolbarVue/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import TopToolbarVue from './components/TopToolbar.vue'
export default {
  components:{
    TopToolbarVue
  },
  name: 'App',

  data: () => ({
    //
  })
}
</script>
