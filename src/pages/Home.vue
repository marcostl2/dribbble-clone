<template>
  <v-container fluid>
    <NavBar />
    <CategoriesAndFilters />
    <v-layout>
      <v-row class="d-flex flex-column justify-center">
        <p class="text-h4 text-center font-weight-bold" style="color:#333">
          You aren’t following anyone yet
        </p>
        <p class="text-center">
          <a style="color: #ea4c89">Find friends</a> you already know from
          Twitter.
        </p>
      </v-row>
    </v-layout>
    <Gallery />
  </v-container>
</template>

<script>
import NavBar from "../components/NavBar";
import CategoriesAndFilters from "../components/CategoriesAndFilters";
import Gallery from "../components/Gallery";

export default {
  components: {
    NavBar,
    Gallery,
    CategoriesAndFilters,
  },
};
</script>

<style></style>
