<template>
  <div id="layout" :class="[menuStatus ? 'close' : 'open']">
    <LayoutHeader />
    <LayoutMain />
    <LayoutNav />
  </div>
</template>
<script>
import LayoutHeader from "./Components/Header";
import LayoutMain from "./Components/Main";
import LayoutNav from "./Components/Nav";
// import { LayoutHeader, LayoutMain, LayoutNav } from './Components'
export default {
  name: "layout",
  components: { LayoutHeader, LayoutMain, LayoutNav },
  computed: {
    menuStatus() {
      return this.$store.state.app.isCollapse;
    }
  }
};
</script>
<style lang="scss" scoped></style>