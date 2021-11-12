<template>
  <section class="calendarios" col lg="9">
    <h3 class="box-content text-center">CALENDÁRIOS</h3>
    <PriceSet>
      <p class="box-content">
        <IconArrowRight /><b>Valor: R$160,00</b>
        <br />
        <IconArrowRight />Os calendários podem ser temáticos. Criamos e
        confeccionamos a partir da escolha do cliente.
        <br />
        <IconArrowRight />Contém 31 dias, 12 meses, 03 anos, estações do ano,
        tempo e humor + saquinho para guardar meses e anos.
        <br />
        <IconArrowRight />Dimensões: 50cm x 50cm
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="calendarios" />
  </section>
</template>

<script>
import { calendarios } from "@/assets/js/calendarios.js";

export default {
  name: "Calendarios",
  data() {
    return {
      calendarios: calendarios,
    };
  },
};
</script>