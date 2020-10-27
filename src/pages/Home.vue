<template>
  <v-container fluid class="pa-0">
    <NavBar />
    <CategoriesAndFilters />
    <v-layout class="pa-0 px-6 px-md-12" column>
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
    </v-layout>
    <Footer />
  </v-container>
</template>

<script>
import NavBar from "../components/NavBar";
import CategoriesAndFilters from "../components/CategoriesAndFilters";
import Gallery from "../components/Gallery";
import Footer from "../components/Footer";

export default {
  components: {
    NavBar,
    Gallery,
    Footer,
    CategoriesAndFilters,
  },
};
</script>

<style></style>
