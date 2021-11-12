<template>
  <section class="mobiles" col lg="9">
    <h3 class="box-content text-center">MÓBILES</h3>
    <PriceSet>
      <p class="box-content">
        <IconArrowRight />Móbile Frida Kahlo - <b>Valor: R$130,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="mobiles" />
  </section>
</template>

<script>
import { mobiles } from "@/assets/js/mobiles.js";

export default {
  name: "Mobiles",
  data() {
    return {
      mobiles: mobiles,
    };
  },
};
</script>