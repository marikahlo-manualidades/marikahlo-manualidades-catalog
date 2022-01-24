<template>
  <section class="calendarios" col lg="9">
    <BoxContent compType="h3" class="text-center">CALENDÁRIOS</BoxContent>
    <ProductInfo :produto="calendarios" />
  </section>
</template>

<script>
import { calendarios } from "@/assets/js/calendarios.js";

export default {
  name: "Calendarios",
  data() {
    return {
      calendarios,
    };
  },
};
</script>