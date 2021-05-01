<template>
  <v-card height="unset" width="100%" class="mx-auto aside">
    <img :src="logo" alt="Quiteja" class="logo-quiteja" />
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      logo: "./img/quiteja-oficial.png",
    };
  },
};
</script>

<style lang="scss" scoped>
.v-sheet.v-card {
  border-radius: 0;
}

.aside {
  display: flex;
  justify-content: center;
  align-items: center;

  .logo-quiteja {
    padding: 16px 0;
  }
}
</style>
