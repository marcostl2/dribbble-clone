<template>
  <v-footer class="px-8 footer pt-12">
    <v-layout column>
      <v-flex class="mb-4">
        <v-img src="../assets/dribbble.svg" contain width="100"></v-img>
      </v-flex>
      <v-flex>
        <p>
          Dribbble is the world’s leading community for creatives to share,
          grow, and get hired.
        </p>
      </v-flex>
      <v-flex class="d-flex">
        <v-img
          src="https://img.icons8.com/wired/64/000000/dribbble.png"
          contain
          max-width="20"
        />
        <v-icon>mdi-twitter</v-icon>
        <v-icon>mdi-facebook</v-icon>
        <v-icon>mdi-instagram</v-icon>
        <v-icon>mdi-pinterest</v-icon>
      </v-flex>
      <v-row class="footer-links pb-8 d-flex wrap">
        <v-col cols="6" md="3">
          <div class="d-flex flex-column">
            <h4>For designers</h4>
            <a>Go Pro!</a>
            <a>Explore design work</a>
            <a>Design blog</a>
            <a>Overtime podcast</a>
            <a>Dribbble meetups</a>
            <a>Playoffs</a>
            <a>Weekly Warm-up</a>
            <a>Code of conduct</a>
          </div>
        </v-col>
        <v-col cols="6" md="3">
          <div class="d-flex flex-column">
            <h4>Hire designers</h4>
            <a>Post a job opening</a>
            <a>Post a freelance project</a>
            <a>Search for designers</a>
            <h4 class="mt-6">Brands</h4>
            <a>Advertise with us</a>
          </div>
        </v-col>
        <v-col cols="6" md="3">
          <div class="d-flex flex-column">
            <h4>Company</h4>
            <a>About</a>
            <a>Careers</a>
            <a>Support</a>
            <a>Media kit</a>
            <a>Dribbble shop</a>
            <a>Testmonials</a>
            <a>API</a>
            <a>Terms of service</a>
            <a>Privacy policy</a>
          </div>
        </v-col>
        <v-col cols="6" md="3">
          <div class="d-flex flex-column">
            <h4>Company</h4>
            <a>Top designers</a>
            <a>Top design teams</a>
            <a>Design jobs</a>
            <a>Tags</a>
            <a>Places</a>
            <h4 class="mt-6">Design assets</h4>
            <a>Shop Creative Market</a>
          </div>
        </v-col>
      </v-row>
      <v-flex class="d-flex align-center flex-column footer-rights py-8">
        <p>© 2020 Dribbble. All rights reserved.</p>
        <p>Made with ♥ remotely from</p>
        <p>Três lagoas, Brasil</p>
        <v-img
          contain
          max-width="30"
          class="my-2"
          src="https://img.icons8.com/offices/64/000000/dribbble.png"
        />
        <p><strong class="black--text">14,454,900</strong> shots dribbbled</p>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.footer-links {
  border-bottom: 1px solid #e7e7e9;
}
.v-icon {
  margin-left: 10px !important;
}
a {
  color: #3d3d4e !important;
  text-decoration: none;
  margin: 6px 0;
}
.footer-rights {
  color: #6e6d7a;

  p {
    margin: 0;
  }
}
</style>
