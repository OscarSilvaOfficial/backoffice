<template>
  <v-card height="unset" width="100%" class="mx-auto aside">
    <v-btn class="btn-close" @click="changeMenuState()" icon>
      <v-icon>mdi-window-close</v-icon>
    </v-btn>
    <img :src="logo" alt="Quiteja" class="logo-quiteja" />
  </v-card>
</template>

<script>
import $ from "jquery";

export default {
  data() {
    return {
      logo: "./img/quiteja-oficial.png",
      isOpen: true,
    };
  },

  methods: {
    changeMenuState() {
      if (this.isOpen) {
        $(".aside").addClass("active");
      } else {
        $(".aside").removeClass("active");
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.v-sheet.v-card {
  border-radius: 0;
}

.active {
  width: 20%;
}

.aside {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 16px 22px;
  flex-direction: column;
  position: relative;
  transition: width 5s;

  .btn-close {
    margin-left: auto;
  }

  .logo-quiteja {
    padding: 16px 0;
    width: 100%;
  }
}
</style>
