<template>
  <v-container>
    <v-app-bar flat app color="#FFF">
      <v-layout>
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
          <v-row @mouseover="option = 1" @mouseleave="option = 0">
            <v-btn small color="#7F7B7B" text
              >Explore <v-icon>mdi-chevron-down</v-icon></v-btn
            >
          </v-row>
          <v-row @mouseover="option = 2" @mouseleave="option = 0">
            <v-btn small color="#7F7B7B" text
              >For Designers <v-icon>mdi-chevron-down</v-icon></v-btn
            >
          </v-row>
          <v-row style="color:#7F7B7B">
            |
          </v-row>
          <v-row @mouseover="option = 3" @mouseleave="option = 0">
            <v-btn small color="#7F7B7B" text
              >Hiring Designers?<v-icon>mdi-chevron-down</v-icon></v-btn
            >
          </v-row>
        </v-layout>
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
              class="btn-search"
              :hide-details="true"
              style="border-radius:10px"
            ></v-text-field>
            <v-btn small text><v-icon>mdi-briefcase</v-icon></v-btn>
            <v-avatar class="mr-4">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
            </v-avatar>
            <v-btn color="#ea4c89" class="white--text">Upload</v-btn>
          </v-row>
          <v-row> </v-row>
        </v-layout>
      </v-layout>
    </v-app-bar>
    <v-app-bar absolute style="top:64px" flat app v-if="option == 1">
      <p>JFEJKEFKJFKFEKLFE</p>
    </v-app-bar>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      option: 0,
    };
  },
};
</script>

<style lang="scss">
// .btn-search {
//   max-height: 30px !important;

//   input {
//     margin: 0 !important;
//   }
//   .v-input__prepend-inner {
//     margin: 0 !important;
//   }
// }
// .v-text-field__slot,
// .v-input__slot {
//   max-height: 30px !important;
// }
</style>
