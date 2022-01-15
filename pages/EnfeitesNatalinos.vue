<template>
  <section class="enfeites-natalinos" col lg="9">
    <h3 class="box-content text-center">ENFEITES NATALINOS</h3>
    <PriceSet>
      <h5 class="box-content text-center">PORTA TALHERES</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor unitário: R$8,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="portaTalheres" />
    <PriceSet>
      <h5 class="box-content text-center">GUIRLANDAS NATALINAS</h5>
    </PriceSet>
    <CatalogMasonry :produtos="guirlanda" tipo="cards" />
  </section>
</template>

<script>
import { portaTalheres, guirlanda } from "@/assets/js/enfeites-natalinos.js";
export default {
  name: "EnfeitesNatalinos",
  data() {
    return {
      guirlanda: guirlanda,
      portaTalheres: portaTalheres,
    };
  },
};
</script>

<style scoped>
section > div:nth-child(4) > h5 {
  margin-bottom: 10px;
}
</style>
