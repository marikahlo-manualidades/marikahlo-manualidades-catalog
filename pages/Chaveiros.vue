<template>
  <section class="chaveiros">
    <BoxContent compType="h3" class="text-center">CHAVEIROS</BoxContent>
    <ProductInfo :produto="chaveiros" tipo="cards" />
  </section>
</template>

<script>
import { chaveiros } from "@/assets/js/chaveiros.js";

export default {
  name: "Chaveiros",
  data() {
    return {
      chaveiros,
    };
  },
};
</script>
