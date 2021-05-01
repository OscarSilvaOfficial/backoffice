<template>
  <main class="main">
    <SideMenu />
    <Header />
    <SideHistory />
  </main>
</template>

<script>
import Header from "@/components/Header";
import SideMenu from "@/components/SideMenu";
import SideHistory from "@/components/SideHistory";

export default {
  name: "index",
  components: {
    Header,
    SideMenu,
    SideHistory,
  },
};
</script>

<style lang="scss">
.main {
  display: grid;
  grid-template-columns: 17.5% auto 17.5%;
}
</style>
