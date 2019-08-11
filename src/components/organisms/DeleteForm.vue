<template>
  <v-container fluid grid-list-xl>
    <v-layout wrap align-center>
      <v-flex xs12 sm6 d-flex>
        <v-select :items="items" label="Select 1" outlined disabled></v-select>
      </v-flex>
      <v-flex xs12 sm6 d-flex>
        <v-select :items="items" label="Select 2" outlined disabled></v-select>
      </v-flex>
      <v-flex xs10 offset-xs1>
        <v-btn v-if="!alert" block color="secondary" dark @click="alert = true">Delete</v-btn>
      </v-flex>
    </v-layout>
    <div>
      <v-alert
        v-model="alert"
        border="left"
        close-text="Close Alert"
        color="success"
        dark
        dismissible
      >削除成功</v-alert>
    </div>
  </v-container>
</template> 

<script>
export default {
  name: "DeleteForm",
  data: () => ({
    items: ["a", "b", "c", "d"],
    alert: false
  })
};
</script>