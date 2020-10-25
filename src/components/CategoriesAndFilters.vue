<template>
  <v-layout column class="px-6 px-md-12">
    <v-flex
      class="d-flex d-md-none justify-space-between py-6"
      style="box-shadow: inset 0px -1px 0px #f3f4f4;"
    >
      <v-select
        style="max-width:120px"
        dense
        hide-details
        append-icon="mdi-chevron-down"
        label="Following"
        outlined
        :items="items"
      ></v-select>
      <v-btn style="max-width:120px" outlined @click="hidden = !hidden"
        ><v-icon>mdi-filter-variant</v-icon>Filters</v-btn
      >
    </v-flex>
    <v-layout class="btn-group py-8" align-center justify-space-between>
      <v-flex class="d-none d-md-flex">
        <v-select
          style="max-width:120px"
          dense
          hide-details
          append-icon="mdi-chevron-down"
          label="Following"
          outlined
          :items="items"
        ></v-select>
      </v-flex>
      <v-flex
        :class="[$vuetify.breakpoint.sm ? 'overflow' : '', 'd-flex nowrap']"
      >
        <v-btn small depressed>All</v-btn>
        <v-btn text small>Animation</v-btn>
        <v-btn text small>Branding</v-btn>
        <v-btn text small>Illustration</v-btn>
        <v-btn text small>Mobile</v-btn>
        <v-btn text small>Print</v-btn>
        <v-btn text small>Product Design</v-btn>
        <v-btn text small>Typography</v-btn>
        <v-btn text small>Web Design</v-btn>
      </v-flex>
      <v-flex class="d-none d-md-flex justify-end">
        <v-btn style="max-width:120px" outlined @click="hidden = !hidden"
          ><v-icon>mdi-filter-variant</v-icon>Filters</v-btn
        >
      </v-flex>
    </v-layout>
    <v-expand-transition>
      <v-layout bottom v-show="!hidden">
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
        <v-flex class="pr-8">
          <span>Color</span>
          <v-text-field
            prepend-inner-icon="mdi-palette"
            dense
            rounded
            filled
            background-color="#f3f3f4"
            placeholder="Enter hex or select"
            :hide-details="true"
            style="border-radius:10px;box-shadow:none !important;"
          >
          </v-text-field>
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

<style lang="scss" scoped>
.v-btn {
  text-transform: none !important;
  text-decoration: capitalize !important;
  font-weight: 400;
  font-size: 14px;
  padding: 0 10px !important;
  color: #6e6d7a !important;
}
.overflow {
  overflow-y: scroll;
}
</style>
