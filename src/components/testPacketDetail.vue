<template>
  <div
    class="testPacketDetail-section row flex flex-align-center flex-justify-center flex-dir-col"
  >
    <h2 class="testPacketDetail-title center">{{ title }}</h2>
    <div class="col-sm-12 w-100 flex testPacketDetail-details ">
      <div
        class="testPacketDetail-content col-sm-6 col-12 flex flex-justify-start flex-align-start flex-dir-row"
        v-for="testPacket in testPacket_list"
        v-bind:key="testPacket.title"
      >
        <div class="col-4">
          <img :src="testPacket.src" :alt="testPacket.alt" />
        </div>
        <div class="col-8">
          <h6>{{ testPacket.title }}</h6>
          <ul class="flex w-100 testPacketDetail-desc flex-dir-col">
            <li
              class=""
              v-for="details in testPacket.details"
              v-bind:key="details"
            >
              <p>{{ details }}</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Dein Testpaket enthält",
      testPacket_list: [
        {
          title: "10 LILLYDOO WINDELN",
          details: [
            "0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz",
            "Extra weich und super bequem",
            "Mit unseren Turbo Tunneln für eine ideale Passform und schnelle Absorption"
          ],
          src:
            "/assets/desktop/lillydoo-little-blowballs-design-preview-tp.png",
          alt: "10 LILLYDOO WINDELN"
        },
        {
          title: "15 FEUCHTTÜCHER MIT 99 % WASSER",
          details: [
            "0 % Parfüme & PEGs, 100 % biologisch abbaubar",
            "Natürlich rein, extra mild, Alternative zu 'Wasser & Watte'"
          ],
          src: "/assets/desktop/water-wipes-15-small.png",
          alt: "15 FEUCHTTÜCHER MIT 99 % WASSER"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
@import "../styles/components/_testPacketDetail.scss";
</style>
