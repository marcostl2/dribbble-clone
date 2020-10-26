<template>
  <div>
    <v-layout
      row
      align-center
      class="px-44 d-flex nowrap justify-space-between"
      style="box-shadow: inset 0px -1px 0px #f3f4f4;"
    >
      <v-row class="d-none d-md-flex justify-space-between align-center px-14">
        <v-col cols="6" class="d-flex align-center">
          <v-img src="../assets/dribbble.svg" max-width="80" contain></v-img>
          <v-btn
            @mouseover="option = 1"
            @mouseleave="option = 0"
            small
            color="#7F7B7B"
            text
            height="100%"
            class="text-capitalize text-subtitle-2 font-weight-bold py-4"
            >Explore <v-icon>mdi-chevron-down</v-icon></v-btn
          >
          <v-btn
            @mouseover="option = 1"
            @mouseleave="option = 0"
            small
            color="#7F7B7B"
            text
            height="100%"
            class="text-capitalize text-subtitle-2 font-weight-bold"
            >For Designers <v-icon>mdi-chevron-down</v-icon></v-btn
          >
          |
          <v-btn
            @mouseover="option = 1"
            @mouseleave="option = 0"
            x-small
            color="#7F7B7B"
            text
            height="100%"
            min-height="70"
            class="text-capitalize text-subtitle-2 font-weight-bold"
            >Hiring Designers?<v-icon>mdi-chevron-down</v-icon></v-btn
          >
        </v-col>
        <v-col cols="5" class="d-flex align-center">
          <v-btn small text color="#bb3d6e">{{
            $vuetify.breakpoint.lg ? "Upgrade Now - Go Pro" : "Go Pro"
          }}</v-btn>
          <v-text-field
            prepend-inner-icon="mdi-magnify"
            placeholder="Search"
            rounded
            dense
            filled
            background-color="#f3f3f4"
            color="#6e6d7a"
            :hide-details="true"
            style="border-radius:10px;box-shadow:none !important;"
          ></v-text-field>
          <v-menu open-on-hover offset-y>
            <template v-slot:activator="{ on, attrs }">
              <v-btn v-bind="attrs" v-on="on" small text
                ><v-icon>mdi-briefcase</v-icon></v-btn
              >
            </template>
            <v-card width="400">
              <v-layout column class="pa-3">
                <v-flex class="d-flex justify-space-around align-center">
                  <span>Not available</span>
                  <v-switch color="#ea4c89" inset></v-switch>
                  <span>Available for work</span>
                </v-flex>
                <v-flex class="d-flex justify-center align-center my-3">
                  <hr width="90%" />
                </v-flex>
                <v-flex class="d-flex justify-center align-center">
                  <span>Edit work availability</span>
                </v-flex>
              </v-layout>
            </v-card>
          </v-menu>
          <div class="d-none d-md-flex">
            <v-avatar class="mr-4" size="36">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
            </v-avatar>
            <v-btn
              depressed
              color="#ea4c89"
              style="border-radius:8px"
              class="white--text text-capitalize text-subtitle-1 font-weight-bold"
              >Upload</v-btn
            >
          </div>
        </v-col>
      </v-row>
    </v-layout>
    <v-app-bar style="top:70px;" height="200" flat app v-if="option == 1">
      <v-layout row align-center>
        <v-row class="px-12">
          <NavBarItem />
          <NavBarItem />
          <NavBarItem />
          <NavBarItem />
        </v-row>
      </v-layout>
    </v-app-bar>
  </div>
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

<style></style>
