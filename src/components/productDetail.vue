<template>
  <div class="productDetail-section row" id="productDetail">
    <div class="col-lg-7 col productDetail-imgSection d-none d-lg-block">
      <img
        :src="logoSrc"
        class="productDetail-logo"
        contain
        :alt="logoAlt"
      />
      <img
        :src="currBackgroundSrc"
        class="productDetail-img"
        contain
        :alt="currBackgroundAlt"
      />
    </div>
    <div class="col-lg-5 colproductDetail-content">
      <h2>
        Unser gratis Testpaket
      </h2>
      <div class="productDetail-size">
        <h3 class="uppercase">Wähle Deine Grössednmendne</h3>
        <ul class="productDetail-controls">
          <li
            class="btn btn-secondary"
            :class="{ active: activeIndex === index }"
            v-on:click="nextImage(item, index)"
            v-for="(item, index) in item_list"
            v-bind:key="item.title"
          >
            <p>{{ item.title }}</p>
            <span>{{ item.weight }}</span>
          </li>
        </ul>
      </div>
      <div class="productDetail-mobileImages d-lg-none d-xl-none">
       <img
        :src="logoSrc"
        class="productDetail-logo"
        contain
        :alt="logoAlt"
      />
        <img
          :src="currBackgroundSrc"
          class="productDetail-img"
          contain
          :alt="currBackgroundAlt"
        />
      </div>
      <div class="productDetail-additionaInformation">
        <p>
          Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere
          Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven
          Feuchttücher zu Größe 4 - 5. Wir zahlen die Produkte, Du nur den
          Versand.
        </p>
        <ul>
          <li class="highlight">
            Automatischer Übergang ins jederzeit kündbare Windel-Abo für 49,50 €
            pro Lieferung.
          </li>
          <li>
            Preise inkl. MwSt., ggf. zzgl.
            <a href="/" class="highlight"> shipping costs</a> Versandkosten
          </li>
        </ul>
        <a href="/" class="btn btn-primary w-100">In den Warenkorb legen</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currBackgroundSrc: "../assets/desktop/lillydoo-testpaket-10.jpg",
      currBackgroundAlt: "lillydoo-testpaket-10",
      logoSrc:'../assets/icons/oekotex_green_de.svg',
      logoAlt:"Oeko-Tex Certificate",
      activeIndex: 0,
      item_list: [
        {
          title: "1",
          weight: "(2-3 KG)",
          src: "/assets/desktop/lillydoo-testpaket-10.jpg",
          alt: "lillydoo-testpaket-10"
        },
        {
          title: "2",
          weight: "(3-4 KG)",
          src: "/assets/desktop/lillydoo-testpaket-20.jpg",
          alt: "lillydoo-testpaket-20"
        },
        {
          title: "3",
          weight: "(4-7 KG)",
          src: "/assets/desktop/lillydoo-testpaket-30.jpg",
          alt: "lillydoo-testpaket-30"
        },
        {
          title: "4",
          weight: "(7-10 KG)",
          src: "/assets/desktop/lillydoo-testpaket-40.jpg",
          alt: "lillydoo-testpaket-40"
        },
        {
          title: "5",
          weight: "(10-12 KG)",
          src: "/assets/desktop/lillydoo-testpaket-50.jpg",
          alt: "lillydoo-testpaket-50"
        }
      ]
    };
  },
  methods: {
    nextImage: function(item, index) {
      this.activeIndex = index;
      this.currBackgroundSrc = item.src;
      this.currBackgroundAlt = item.alt;
    }
  }
};
</script>
<style lang="scss" scoped>
@import "../styles/components/_productDetail.scss";
</style>
