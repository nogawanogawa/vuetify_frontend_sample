<template>
  <v-container fluid grid-list-xl>
    <v-layout wrap align-center>
      <v-flex xs12 sm6 d-flex>
        <v-select :items="items" label="Select 1" outlined></v-select>
      </v-flex>
      <v-flex xs12 sm6 d-flex>
        <v-select :items="items" label="Select 2" outlined></v-select>
      </v-flex>
      <v-flex xs10 offset-xs1>
        <v-btn block color="secondary" dark>Search</v-btn>
      </v-flex>
    </v-layout>
  </v-container>
</template>


<script>
export default {
  name: "SearchForm",
  data: () => ({
    items: ["A", "B", "C", "D"]
  })
};
</script>