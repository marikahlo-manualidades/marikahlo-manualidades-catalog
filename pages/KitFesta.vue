<template>
  <section class="kit-festa" col lg="9">
    <BoxContent compType="h3" class="text-center">KIT FESTA</BoxContent>
    <ProductInfo :produto="kitFesta" />
    <ProductInfo :produto="fatiaBolo" />
    <ProductInfo :produto="prato" />
    <ProductInfo :produto="canecaSuco" />
    <ProductInfo :produto="talheres" />
  </section>
</template>

<script>
import {
  kitFesta,
  fatiaBolo,
  prato,
  canecaSuco,
  talheres,
} from "@/assets/js/kit-festa.js";
export default {
  name: "KitFesta",
  data() {
    return {
      kitFesta,
      fatiaBolo,
      canecaSuco,
      prato,
      talheres,
    };
  },
};
</script>

