<template>
  <v-layout
    row
    align-center
    class="px-44 d-flex nowrap justify-space-between px-8"
    style="box-shadow: inset 0px -1px 0px #f3f4f4;"
  >
    <v-row>
      <v-col class="d-flex justify-space-between">
        <v-icon @click="drawer = !drawer">mdi-menu</v-icon>
        <v-img src="../assets/dribbble.svg" max-width="80" contain></v-img>
        <v-icon>mdi-briefcase</v-icon>
      </v-col>
    </v-row>
    <v-navigation-drawer v-model="drawer" absolute bottom temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
    };
  },
  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style></style>
