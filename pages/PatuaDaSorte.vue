<template>
  <section class="patua-da-sorte" col lg="9">
    <BoxContent compType="h3" class="text-center">PATUÁ DA SORTE</BoxContent>
    <ProductInfo :produto="patuaDaSorte" />
  </section>
</template>

<script>
import { patuaDaSorte } from "@/assets/js/patua-da-sorte.js";

export default {
  name: "PatuaDaSorte",
  data() {
    return {
      patuaDaSorte,
    };
  },
};
</script>