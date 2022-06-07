<template>
<div>
    <v-app-bar app color="#323B50">
        <v-toolbar-title class="white--text">Practice</v-toolbar-title> 
    </v-app-bar>
    <v-navigation-drawer app dark color="#323B50" mini-variant mini-variant-width="90">
    <v-avatar class="d-block text-center mx-auto mt-4 border_img" size="40">
        <img style="object-fit: cover" src="../assets/logo.png" alt="">
    </v-avatar>
    <v-list flat class="mt-5">
        <v-list dense>
            <v-list-item :to="{ path: '/' }">
                <v-list-item-action>
                    <v-icon>mdi-laptop</v-icon>
                </v-list-item-action>
            </v-list-item>
            <v-list-item :to="{ path: '/settings' }">
                <v-list-item-action>
                    <v-icon>mdi-cogs</v-icon>
                </v-list-item-action>
            </v-list-item>
            <v-list-item :to=" {path: '/about'} ">
                <v-list-item-action>
                    <v-icon>mdi-cat</v-icon>
                </v-list-item-action>
            </v-list-item>
      </v-list>
    </v-list>
    </v-navigation-drawer>
</div>
</template>

<script>
export default {
    data: () => ({
    })
}
</script>
