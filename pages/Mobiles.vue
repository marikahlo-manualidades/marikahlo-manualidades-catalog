<template>
  <section class="mobiles" col lg="9">
    <h3 class="box-content text-center">GUIRLANDAS E MÓBILES</h3>
    <PriceSet>
      <h5 class="box-content text-center">GUIRLANDA TEMÁTICA</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$180,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="guirlandas" />
    <PriceSet>
      <h5 class="box-content text-center">MÓBILE FRIDA KAHLO</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$130,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="mobiles" />
  </section>
</template>

<script>
import { mobiles, guirlandas } from "@/assets/js/mobiles.js";

export default {
  name: "Mobiles",
  data() {
    return {
      mobiles: mobiles,
      guirlandas: guirlandas,
    };
  },
};
</script>