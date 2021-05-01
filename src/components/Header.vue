<template>
  <v-toolbar id="header" height="unset" dense>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-btn id="icon-bell" icon>
      <v-icon>mdi-bell</v-icon>
    </v-btn>

    <v-avatar>
      <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
    </v-avatar>
  </v-toolbar>
</template>
<style lang="scss" scoped>
#header {
  background-color: #145f6a;
  display: flex;
  align-items: center;
  border-radius: 0;

  #icon-bell {
    margin-left: auto;
  }

  header {
    width: 100%;
  }

  i {
    color: #ffffff;
  }

  @media (min-width: 601px) {
    height: 64px !important;
  }

  @media (max-width: 600px) {
    height: 48px !important;
  }
}
</style>
<script>
import $ from "jquery";

export default {
  mounted() {
    $(".v-toolbar__content").css("width", "100%");
  },
};
</script>
