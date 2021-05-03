<template>
  <v-card height="unset" width="320px" class="mx-auto aside" id="side-menu">
    <picture>
      <img :src="logo" alt="Quiteja" class="logo-quiteja" />
    </picture>
    <Select :selectItems="creditors" />
    <v-btn class="btn-close" v-show="isOpen" @click="changeMenuState()" icon>
      <v-icon>mdi-arrow-left</v-icon>
    </v-btn>
    <v-btn class="btn-close" v-show="!isOpen" @click="changeMenuState()" icon>
      <v-icon>mdi-arrow-right</v-icon>
    </v-btn>
  </v-card>
</template>

<script>
import $ from "jquery";
import Select from "@/components/Select";

export default {
  components: {
    Select,
  },

  data() {
    return {
      logo: "./img/quiteja-oficial.png",
      isOpen: true,
      creditors: ["Bradesco", "MercadoLivre", "Banco Pan"],
    };
  },

  methods: {
    changeMenuState() {
      if (this.isOpen) {
        this.isOpen = false;
        $("#side-menu").css("width", "70px");
        $("#side-menu picture").css("clip-path", "circle(30% at 42% 50%)");
        $(".logo-quiteja").css("left", "49px").css("width", "150px");
      } else {
        this.isOpen = true;
        $("#side-menu").css("width", "320px");
        $("#side-menu picture").css("clip-path", "unset");
        $(".logo-quiteja").css("left", "unset").css("width", "unset");
      }
    },
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
  padding: 16px 0px;
  flex-direction: column;
  transition: all 0.7s;

  picture {
    transition: clip-path 0.7s;

    .logo-quiteja {
      padding: 16px 22px;
      position: relative;
      transition: clip-path 0.7s;
    }
  }
}
</style>
