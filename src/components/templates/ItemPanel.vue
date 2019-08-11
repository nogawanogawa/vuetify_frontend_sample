<template>
  <v-card xs10 color="grey darken-2">
    <v-card-title>ListUp</v-card-title>
    <v-flex v-for="(item, i) in items" :key="i">
      <ItemCard v-bind:title="item.title" v-bind:text="item.text"></ItemCard>
    </v-flex>
  </v-card>
</template>

<script>
import ItemCard from "@/components/organisms/ItemCard.vue";

export default {
  name: "ItemPanel",
  components: {
    ItemCard
  },
  data: () => ({
    items: [
      {
        title: "Item 1",
        text: "Item 1"
      },
      {
        title: "Item 2",
        text: "Item 2"
      }
    ]
  }),
  methods: {
    click() {
      this.$router.push({ path: "/Detail" });
    }
  }
};
</script>

<style scoped>
.v-input__slider {
  width: 100%;
}
</style>