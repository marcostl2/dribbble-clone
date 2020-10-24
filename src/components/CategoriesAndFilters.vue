<template>
  <v-layout column>
    <v-layout class="btn-group py-5">
      <v-flex class="d-flex justify-center">
        <v-select
          style="max-width:120px"
          dense
          append-icon="mdi-chevron-down"
          label="Following"
          outlined
          :items="items"
        ></v-select>
      </v-flex>
      <v-layout>
        <v-flex>
          <v-btn depressed>All</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Animation</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Branding</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Illustration</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Mobile</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Print</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Product Design</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Typography</v-btn>
        </v-flex>
        <v-flex>
          <v-btn text>Web Design</v-btn>
        </v-flex>
      </v-layout>
      <v-flex class="d-flex justify-center">
        <v-btn style="max-width:120px" outlined @click="hidden = !hidden"
          ><v-icon>mdi-filter-variant</v-icon>Filters</v-btn
        >
      </v-flex>
    </v-layout>
    <v-expand-transition>
      <v-layout bottom v-show="!hidden" class="px-12">
        <v-flex class="pr-8">
          <span>Tags</span>
          <v-text-field
            prepend-inner-icon="mdi-magnify"
            dense
            rounded
            filled
            background-color="#f3f3f4"
            color="#6e6d7a"
            :hide-details="true"
            style="border-radius:10px;box-shadow:none !important"
          ></v-text-field>
        </v-flex>
        <v-flex class="pr-8" id="palette-input">
          <span>Color</span>
          <v-text-field
            prepend-inner-icon="mdi-palette"
            dense
            rounded
            filled
            background-color="#f3f3f4"
            color="red"
            placeholder="Enter hex or select"
            :hide-details="true"
            style="border-radius:10px;box-shadow:none !important"
          ></v-text-field>
        </v-flex>
        <v-flex class="pr-8">
          <span>Made With</span>
          <v-select
            dense
            append-icon="mdi-chevron-down"
            label="All Apps"
            outlined
            :items="items"
          ></v-select>
        </v-flex>
        <v-flex>
          <span>Downloads</span>
          <v-select
            dense
            append-icon="mdi-chevron-down"
            label="All Shots"
            outlined
            :items="items"
          ></v-select>
        </v-flex>
      </v-layout>
    </v-expand-transition>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      hidden: true,
      items: ["Following", "Popular", "New & Noteworthy", "Goods for Sale"],
    };
  },
};
</script>

<style lang="scss">
.v-btn {
  text-transform: none !important;
  text-decoration: capitalize !important;
  font-weight: 400;
  padding: 0 10px !important;
}
#palette-input .v-icon {
  color: orangered !important;
}
</style>
