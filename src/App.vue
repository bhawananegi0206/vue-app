<template>
  <div id="app">
    <heroShot></heroShot>
    <productDetail></productDetail>
    <subscriptionDetail></subscriptionDetail>
    <testPacketDetail></testPacketDetail>
  </div>
</template>

<script>
import heroShot from "./components/heroShot";
import productDetail from "./components/productDetail";
import subscriptionDetail from "./components/subscriptionDetail";
import testPacketDetail from "./components/testPacketDetail";

export default {
  name: "App",
  components: { heroShot, productDetail, subscriptionDetail, testPacketDetail }
};
</script>

<style lang="scss" scoped>
#app {
  background: url("/assets/desktop/pusteblume-pattern-04.png") bottom repeat-x;
  padding-bottom: 17rem;
}
</style>
