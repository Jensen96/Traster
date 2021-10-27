<template>
    <v-container>
      <grid
          :entries="gridData"
          :columns="gridColumns"
        >
        </grid>
    </v-container>
</template>

<script>
import Grid from './components/Grid';

export default {
  name: 'App',

  components: {
    Grid,
  },
  props: {
  },

  data: () => ({
    gridColumns: ["name", "brand", "rating", "note", "origin"],
    gridData: [
      { name: "Stout Cask", brand: "Teeling", rating: "8/10", note: "Try the Rum Cask next", origin: "Ireland" },
      { name: "16", brand: "Lagavulin", rating: "6/10", note: "Smokey boy", origin: "Scotland" },
      { name: "Blended Malt", brand: "Monkey Shoulder", rating: "7/10", note: "", origin: "Scotland" }
    ]
  }),
};
</script>

<style lang="scss">
$main-color: #1D1B1B;
$secondary-color: #EC4D37;

body {
  font-family: Helvetica Neue, Arial, sans-serif;
  font-size: 14px;
  color: $secondary-color;
  background-color: $main-color;
}

table {
  border: 2px solid $secondary-color;
  border-radius: 3px;
  background-color: $main-color;
  width: 100%;
  border-collapse: collapse;
}

th {
  background-color: $secondary-color;
  color: $main-color;
}

td {
  background-color: $main-color;
  border: 1px solid $secondary-color;
}

th,
td {
  min-width: 120px;
  padding: 10px 20px;
}

</style>

