<template>
<div class="about">
    <h1>This is a settings page</h1>
    <v-container>
        <v-card dark>
      <v-toolbar flat>
        <v-icon>mdi-account</v-icon>
        <v-toolbar-title class="font-weight-light">
          公司名稱
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn
          color="grey"
          fab
          small
          @click="isEditing = !isEditing"
        >
          <v-icon v-if="isEditing">
            mdi-close
          </v-icon>
          <v-icon v-else>
            mdi-pencil
          </v-icon>
        </v-btn>
      </v-toolbar>
      <v-card-text>
        <v-text-field
          :disabled="!isEditing"
          color="white"
          label="名稱"
        ></v-text-field>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn
          :disabled="!isEditing"
          color="success"
          @click="save"
        >
          儲存
        </v-btn>
      </v-card-actions>
      <v-snackbar
        v-model="hasSaved"
        :timeout="2000"
        color="success"
        absolute
        top
        left
      >
        更新成功!
      </v-snackbar>
        </v-card>
    </v-container>
</div>
</template>
<script>
  export default {
    data: () => ({
        hasSaved: false,
        isEditing: null,
    }),
    methods: {
      save () {
        this.isEditing = !this.isEditing
        this.hasSaved = true
      }
    }
}
</script>
