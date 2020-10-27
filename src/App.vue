<template>
  <v-app>
    <router-view></router-view>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data() {
    return {};
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
.v-application {
  overflow: hidden;
}
.theme--light.v-text-field--outline > .v-input__control > .v-input__slot {
  border: 1px solid !important;
}
</style>
