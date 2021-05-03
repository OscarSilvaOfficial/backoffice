<template>
  <v-col data-app class="d-flex" id="creditor-content">
    <v-select :items="selectItems" id="select-content"></v-select>
  </v-col>
</template>
<script>
export default {
  props: ["selectItems"],
};
</script>
<style lang="scss" scoped>
.d-flex {
  width: 100%;
}

#select-content {
  color: rgba(0, 0, 0, 0.87) !important;
  font-size: 24px !important;
  font-weight: 500 !important;
  text-align: center !important;
}

#creditor-content {
  background-color: #2de587;
}
</style>
