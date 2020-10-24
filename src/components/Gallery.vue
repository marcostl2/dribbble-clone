<template>
  <v-layout column>
    <v-row justify="center">
      <p>Check out some of today’s popular shots</p>
    </v-row>
    <v-row>
      <v-card>
        <v-img src="https://via.placeholder.com/270x200"></v-img>
        <v-card-actions>
          <v-avatar size="28">
            <v-img src="https://via.placeholder.com/40"></v-img>
          </v-avatar>
          <span>Nome do cara</span>
          <span class="user-tag">PRO</span>
          <v-spacer></v-spacer>
          <v-icon>mdi-chat</v-icon>
          <span>20</span>
          <v-icon>mdi-heart</v-icon>
          <span>12</span>
        </v-card-actions>
      </v-card>
    </v-row>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      images: [
        "https://via.placeholder.com/100",
        "https://via.placeholder.com/100",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.user-tag {
  color: white;
  padding: 0 6px;
  border-radius: 5px;
  background: rgb(156, 154, 154);
}
</style>
