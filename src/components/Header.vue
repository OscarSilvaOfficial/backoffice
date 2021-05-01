<template>
  <v-toolbar id="menu-header" height="unset" dense>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-btn id="icon-bell" icon>
      <v-icon>mdi-bell</v-icon>
    </v-btn>
  </v-toolbar>
</template>
<style lang="scss" scoped>
#menu-header {
  background-color: #145f6a;
  display: flex;
  align-items: center;
  border-radius: 0;

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
