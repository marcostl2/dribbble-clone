<template>
  <v-layout column class="pa-0" justify-space-between>
    <v-flex>
      <p class="font-weight-bold mt-15">
        Check out some of today’s popular shots
      </p>
    </v-flex>
    <v-layout wrap justify-space-between>
      <v-row>
        <CardGallery v-for="(Card, i) in gallery" :key="i"> </CardGallery>
      </v-row>
    </v-layout>
    <v-flex v-if="!loading" class="d-flex justify-center my-10">
      <v-btn
        @click="
          gallery.push(CardGallery, CardGallery, CardGallery, CardGallery)
        "
        color="#f3f3f4"
        large
        depressed
        class="font-weight-bold px-12"
        >Load more Shots</v-btn
      >
    </v-flex>
    <v-flex v-else class="d-flex justify-center align-center" id="loading-bkp">
      <v-img
        contain
        max-width="22"
        class="mr-2"
        src="https://img.icons8.com/offices/64/000000/dribbble.png"
      />
      <span>Loading more...</span>
    </v-flex>
  </v-layout>
</template>

<script>
import CardGallery from "./CardGallery";

export default {
  components: {
    CardGallery,
  },
  data() {
    return {
      loading: true,
      gallery: [
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
        CardGallery,
      ],
    };
  },
  mounted: function() {
    window.onscroll = () => {
      let element = document.querySelector("#loading-bkp").offsetTop;
      let pos = window.pageYOffset;

      if (this.gallery.length <= 28) {
        if (pos * 2 + 300 >= element) {
          this.gallery.push(
            CardGallery,
            CardGallery,
            CardGallery,
            CardGallery,
            CardGallery,
            CardGallery,
            CardGallery,
            CardGallery
          );
        }
      } else {
        this.loading = !this.loading;
      }
    };
  },
};
</script>

<style lang="scss" scoped>
.card-info .v-icon + span {
  font-size: 13px;
}
</style>
