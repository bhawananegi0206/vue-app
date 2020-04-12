<template>
  <div
    class="subscriptionDetail-section row flex flex-align-center flex-justify-center"
  >
    <h2 class="subscriptionDetail-title center">{{ title }}</h2>
    <ul class="flex w-100 subscriptionDetail-container">
      <li
        class="subscriptionDetail-content col-sm-4 co-xs-12 flex flex-justify-start flex-align-center flex-dir-col"
        v-for="subscription in subscription_list"
        v-bind:key="subscription.title"
      >
        <img :src="subscription.src" :alt="subscription.alt" />
        <h4>{{ subscription.title }}</h4>
        <p class="center" v-html="subscription.desc"></p>
        <p class="center highlight">{{ subscription.highlight }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Wie es funktioniert",
      subscription_list: [
        {
          title: "DEIN TESTPAKET",
          desc:
            "Wir schenken Dir die Produkte,<br/>Du übernimmst nur das Porto.",
          src: "/assets/icons/lillydoo-your-flexibility-icon.svg",
          alt: "lillydoo-your-flexibility",
          highlight: ""
        },
        {
          title: "DEINE FLEXIBILITÄT",
          desc:
            "Erste Monatsbox nach 14 Tagen für 49,50 € <br/>erhalten. Oder noch vor der ersten Lieferung kündigen.",
          src: "/assets/icons/lillydoo-your-subscription-icon.svg",
          alt: "DEINE FLEXIBILITÄT",
          highlight: "Erfahre hier mehr über das LILLYDOO Windel-Abo."
        },
        {
          title: "DEINE MONATSBOX",
          desc:
            "Jederzeit Windelgröße, Designs und Lieferintervalle <br/>anpassen oder weitere Produkte hinzufügen.",
          src: "/assets/icons/lillydoo-your-trialbox-icon.svg",
          alt: "DEINE MONATSBOX",
          highlight: ""
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
@import "../styles/components/_subscriptionDetail.scss";
</style>
