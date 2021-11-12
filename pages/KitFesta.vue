<template>
  <section class="kit-festa" col lg="9">
    <h3 class="box-content text-center">KIT FESTA</h3>
    <PriceSet>
      <p class="box-content">
        <IconArrowRight/>
        Kit Bolo Com 6 Fatias, 2 Canecas (Com Suco de Laranja ou de Uva), 2
        Garfos, 2 Facas, 2 Pratos e Vela - <b>Valor: R$140,00</b>
        <br />
        <IconArrowRight/>
        Obs: o bolo pode ser feito com sabores e decorações diferentes, conforme
        a preferência.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="kitFesta" />
    <PriceSet>
      <h5 class="box-content text-center">ITENS FESTA</h5>
    </PriceSet>
    <CatalogMasonry :produtos="itensFesta" tipo="cards" />
  </section>
</template>

<script>
import { kitFesta, itensFesta } from "@/assets/js/kit-festa.js";
export default {
  name: "KitFesta",
  data() {
    return {
      kitFesta: kitFesta,
      itensFesta: itensFesta,
    };
  },
};
</script>

<style scoped>
.kit-festa h5 {
  margin-bottom: 10px;
}
</style>