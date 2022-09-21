<template>
  <section class="quadros-rotina" col lg="9">
    <BoxContent compType="h3" class="text-center">QUADROS DE ROTINA</BoxContent>
    <ProductInfo :produto="quadrosRotina" />
  </section>
</template>

<script>
import { quadrosRotina } from "@/assets/js/quadros-rotina.js";

export default {
  name: "QuadrosRotina",
  data() {
    return {
      quadrosRotina,
    };
  },
};
</script>