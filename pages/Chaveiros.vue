<template>
  <section class="chaveiros">
    <h3 class="box-content text-center">CHAVEIROS</h3>
    <PriceSet>
      <p class="box-content">
        <IconArrowRight /><b>Valor unitário: R$4,50</b> – Quantidade mínima para
        pedido: 10 unidades.
        <br />
        <IconArrowRight />Obs: Para pedidos acima de 20 unidades => valor
        unitário a combinar.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="chaveiros" tipo="cards" />
  </section>
</template>

<script>
import { chaveiros } from "@/assets/js/chaveiros.js";

export default {
  name: "Chaveiros",
  data() {
    return {
      chaveiros: chaveiros,
    };
  },
};
</script>
