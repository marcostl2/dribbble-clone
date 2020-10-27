<template>
  <v-layout
    row
    align-center
    class="px-4 d-flex nowrap justify-space-between px-8"
    style="box-shadow: inset 0px -1px 0px #f3f4f4;"
  >
    <v-row>
      <v-col class="d-flex justify-space-between">
        <v-icon @click="drawer = !drawer">mdi-menu</v-icon>
        <v-img src="../assets/dribbble.svg" max-width="80" contain></v-img>
        <v-icon>mdi-briefcase</v-icon>
      </v-col>
    </v-row>
    <v-layout class="px-3" column>
      <v-row>
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
        <v-select
          class="dropdown-option"
          readonly
          hide-details
          color="transparent"
          placeholder="Explore"
          rounded
        ></v-select>
        <v-select
          rounded
          class="dropdown-option"
          readonly
          hide-details
          color="transparent"
          placeholder="For Designers?"
        ></v-select>
        <v-select
          rounded
          class="dropdown-option"
          readonly
          hide-details
          color="transparent"
          placeholder="Hiring Designers?"
        ></v-select>
        <v-select
          rounded
          class="dropdown-option"
          readonly
          hide-details
          color="transparent"
          placeholder="Upload a Shot"
        ></v-select>
      </v-row>
      <v-row>
        <hr />
      </v-row>
      <v-row>
        <v-col class="d-flex align-center">
          <v-avatar class="mr-4" size="36">
            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
          </v-avatar>
          <span>Nome do cara</span>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="6" class="d-flex flex-column">
          <p>Profile</p>
          <p>Work Availability</p>
          <p>Go Pro</p>
        </v-col>
        <v-col cols="6" class="d-flex flex-column">
          <p>My Boosted Shots</p>
          <p>My Likes</p>
          <p>My Collections</p>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="d-flex flex-column ">
          <p>Account Settings</p>
          <p>Sign Out</p>
        </v-col>
      </v-row>
    </v-layout>
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

<style scoped lang="scss">
#first-dropdown {
  border-left: 1px solid #e7e7e9;
  .flex {
    margin-top: 25px;
  }
}
</style>
