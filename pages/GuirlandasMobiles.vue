<template>
  <section class="mobiles" col lg="9">
    <BoxContent compType="h3" class="text-center mb-2"
      >GUIRLANDAS E MÓBILES</BoxContent
    >
    <ProductInfo :produto="guirlandaBoasVindas" />
    <ProductInfo :produto="guirlandaTematica" />
    <ProductInfo :produto="mobileFrida" />
  </section>
</template>

<script>
import {
  mobileFrida,
  guirlandaTematica,
  guirlandaBoasVindas,
} from "@/assets/js/guirlandas-mobiles.js";

export default {
  name: "GuirlandasMobiles",
  data() {
    return {
      mobileFrida,
      guirlandaTematica,
      guirlandaBoasVindas,
    };
  },
};
</script>