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
      <h5 class="box-content text-center">GUIRLANDA</h5>
      <p class="box-content">
       <IconArrowRight />Guirlanda Família Personalizada - <b>Valor: R$150,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="guirlanda" />
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

