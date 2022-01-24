<template>
  <section class="enfeites-natalinos" col lg="9">
    <BoxContent compType="h3" class="text-center mb-2"
      >ENFEITES NATALINOS</BoxContent
    >
    <ProductInfo :produto="portaTalheres" />
    <ProductInfo :produto="guirlandas" tipo="cards" />
  </section>
</template>

<script>
import { portaTalheres, guirlandas } from "@/assets/js/enfeites-natalinos.js";
export default {
  name: "EnfeitesNatalinos",
  data() {
    return {
      guirlandas,
      portaTalheres,
    };
  },
};
</script>

