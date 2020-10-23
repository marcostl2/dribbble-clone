<template>
  <v-container>
    <v-app-bar
      fixed
      app
      color="#FFF"
      style="box-shadow: inset 0px -1px 0px #f3f4f4;"
    >
      <v-layout class="py-5 px-4">
        <v-layout row align-center>
          <v-row>
            <v-btn text
              ><v-img
                src="../assets/dribbble.svg"
                max-width="80"
                contain
              ></v-img
            ></v-btn>
          </v-row>
          <v-row @mouseover="option = 1" @mouseleave="option = 1">
            <v-btn
              small
              color="#7F7B7B"
              text
              class="text-capitalize text-subtitle-1 font-weight-bold"
              >Explore <v-icon>mdi-chevron-down</v-icon></v-btn
            >
          </v-row>
          <v-row @mouseover="option = 1" @mouseleave="option = 0">
            <v-btn
              small
              color="#7F7B7B"
              text
              class="text-capitalize text-subtitle-1 font-weight-bold"
              >For Designers <v-icon>mdi-chevron-down</v-icon></v-btn
            >
          </v-row>
          <v-row style="color:#7F7B7B">
            |
          </v-row>
          <v-row @mouseover="option = 1" @mouseleave="option = 0">
            <v-btn
              small
              color="#7F7B7B"
              text
              class="text-capitalize text-subtitle-1 font-weight-bold"
              >Hiring Designers?<v-icon>mdi-chevron-down</v-icon></v-btn
            >
          </v-row>
        </v-layout>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-layout row align-center>
          <v-row>
            <v-btn small text color="#bb3d6e">Upgrade Now - Go Pro</v-btn>
          </v-row>
          <v-row class="d-flex align-center">
            <v-text-field
              prepend-inner-icon="mdi-magnify"
              label="Search"
              dense
              rounded
              filled
              solo
              background-color="#f3f3f4"
              color="#6e6d7a"
              class="btn-search"
              :hide-details="true"
              style="border-radius:10px;width:100px;box-shadow:none !important"
            ></v-text-field>
            <v-btn small text><v-icon>mdi-briefcase</v-icon></v-btn>
            <v-avatar class="mr-4" size="36">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
            </v-avatar>
            <v-btn
              color="#ea4c89"
              style="border-radius:8px"
              class="white--text text-capitalize text-subtitle-1 font-weight-bold"
              >Upload</v-btn
            >
          </v-row>
        </v-layout>
      </v-layout>
    </v-app-bar>
    <v-app-bar
      style="top:64px;background: url(https://via.placeholder.com/300x140);background-repeat:no-repeat;background-position:right"
      height="200"
      flat
      app
      class="py-3"
      v-if="option == 1"
    >
      <v-layout row align-center class="px-16">
        <NavBarItem />
        <NavBarItem />
        <NavBarItem />
      </v-layout>
    </v-app-bar>
  </v-container>
</template>

<script>
import NavBarItem from "./NavBarItem";
export default {
  components: {
    NavBarItem,
  },
  data() {
    return {
      option: 0,
    };
  },
};
</script>

<style lang="scss">
.v-text-field.v-text-field--solo:not(.v-text-field--solo-flat)
  > .v-input__control
  > .v-input__slot {
  box-shadow: none;
}
</style>
