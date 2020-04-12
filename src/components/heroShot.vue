<template>
  <div class="hero-shot-section flex flex-justify-end">
    <div
      class="hero-shot-overlay flex flex-justify-center flex-align-center flex-dir-col"
    >
      <h1 class="center" v-html="heroTitle"></h1>
      <a href="#productDetail" class="btn btn-primary">{{ heroButtonText }}</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      heroTitle: "Entdecke unsere <br/> Hautfreundlichkeit",
      heroButtonText: "Wähle Deine Grösse"
    };
  }
};
</script>
<style lang="scss" scoped>
@import "../styles/components/_heroShot.scss";
</style>
