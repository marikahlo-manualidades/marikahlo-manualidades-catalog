<template>
  <section class="toalhinhas" col lg="9">
    <BoxContent compType="h3" class="text-center">TOALHINHAS</BoxContent>
    <ProductInfo :produto="toalhinhas" />
  </section>
</template>

<script>
import { toalhinhas } from "@/assets/js/toalhinhas.js";

export default {
  name: "Toalhinhas",
  data() {
    return {
      toalhinhas,
    };
  },
};
</script>