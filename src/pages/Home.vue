<template>
  <v-container>
    <NavBar />
    <Filters />
  </v-container>
</template>

<script>
import NavBar from "../components/NavBar";
import Filters from "../components/Filters";

export default {
  components: {
    NavBar,
    Filters,
  },
};
</script>

<style></style>
