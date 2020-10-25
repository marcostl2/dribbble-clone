<template>
  <v-col cols="12" sm="6" md="3">
    <v-card elevation="0">
      <v-hover v-slot="{ hover }">
        <v-img src="https://picsum.photos/270/200">
          <div
            v-if="hover"
            :class="[{ 'on-hover': hover }, 'px-4 d-flex align-end pb-4']"
          >
            <span class="white--text font-weight-bold">Podcast App</span>
            <div>
              <v-btn v-if="hover" class="pl-1 pr-1" small min-width="10">
                <v-icon color="#6e6d7a">mdi-folder-plus</v-icon>
              </v-btn>
              <v-btn class="pl-1 pr-1 ml-2" v-if="hover" small min-width="10">
                <v-icon color="#6e6d7a">mdi-heart</v-icon>
              </v-btn>
            </div>
          </div>
        </v-img>
      </v-hover>
      <v-card-actions class="card-info">
        <v-avatar size="28">
          <v-img src="https://cdn.vuetifyjs.com/images/john.jpg"></v-img>
        </v-avatar>
        <span class="ml-1 font-weight-bold">Nome do cara</span>
        <span class="user-tag font-weight-bold ml-1">PRO</span>
        <v-spacer></v-spacer>
        <v-icon size="18">mdi-chat</v-icon>
        <span>20</span>
        <v-icon class="ml-1" size="18">mdi-heart</v-icon>
        <span>12</span>
      </v-card-actions>
    </v-card>
  </v-col>
</template>

<script>
export default {};
</script>

<style scoped>
.user-tag {
  font-size: 12px;
  color: white;
  padding: 1px 4px;
  border-radius: 5px;
  background: #ccc;
}
.on-hover {
  justify-content: center;
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
  animation: show-card-links 0.3s;
  background: linear-gradient(
    180deg,
    transparent 62%,
    rgba(0, 0, 0, 0.00345888) 63.94%,
    rgba(0, 0, 0, 0.014204) 65.89%,
    rgba(0, 0, 0, 0.0326639) 67.83%,
    rgba(0, 0, 0, 0.0589645) 69.78%,
    rgba(0, 0, 0, 0.0927099) 71.72%,
    rgba(0, 0, 0, 0.132754) 73.67%,
    rgba(0, 0, 0, 0.177076) 75.61%,
    rgba(0, 0, 0, 0.222924) 77.56%,
    rgba(0, 0, 0, 0.267246) 79.5%,
    rgba(0, 0, 0, 0.30729) 81.44%,
    rgba(0, 0, 0, 0.341035) 83.39%,
    rgba(0, 0, 0, 0.367336) 85.33%,
    rgba(0, 0, 0, 0.385796) 87.28%,
    rgba(0, 0, 0, 0.396541) 89.22%,
    rgba(0, 0, 0, 0.4) 91.17%
  );
}
@keyframes show-card-links {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
