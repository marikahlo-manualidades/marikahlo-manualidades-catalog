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
      <h5 class="box-content text-center">PRATO COM UMA FATIA DE BOLO</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$20,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="fatiaBolo" />
    <PriceSet>
      <h5 class="box-content text-center">PRATO</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor Unitário: R$6,00</b><br />
        <IconArrowRight />Prato feito com estrutura em papelão e recoberto com feltro - Dimensão: 19cm de diâmetro
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="prato" />
    <PriceSet>
      <h5 class="box-content text-center">CANECA SUCO</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor Unitário: R$12,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="canecaSuco" />
        <PriceSet>
      <h5 class="box-content text-center">KIT COM GARFO, FACA E COLHER</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$15,00</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="talheres" />

  </section>
</template>

<script>
import { kitFesta, fatiaBolo, prato, canecaSuco, talheres } from "@/assets/js/kit-festa.js";
export default {
  name: "KitFesta",
  data() {
    return {
      kitFesta,
      fatiaBolo,
      canecaSuco,
      prato,
      talheres
    };
  },
};
</script>

