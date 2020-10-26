<template>
  <v-container fluid class="pa-0">
    <DesktopNavBar v-if="$vuetify.breakpoint.mdAndUp" />
    <MobileNavBar v-else />
  </v-container>
</template>

<script>
import DesktopNavBar from "./DesktopNavBar";
import MobileNavBar from "./MobileNavBar";

export default {
  components: {
    DesktopNavBar,
    MobileNavBar,
  },
};
</script>

<style lang="scss" scoped>
.v-text-field.v-text-field--solo:not(.v-text-field--solo-flat)
  > .v-input__control
  > .v-input__slot {
  box-shadow: none;
}

.v-text-field {
  max-width: 160px;
}
span {
  color: #6e6d7a;
}
</style>
