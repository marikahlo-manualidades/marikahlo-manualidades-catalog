<template>
  <section class="livros-sensoriais" col lg="9">
    <BoxContent compType="h3" class="text-center mb-2"
      >LIVROS SENSORIAIS</BoxContent
    >
    <ProductInfo :produto="livroAtivDiv" />
    <ProductInfo :produto="livroAtivDiv2" />
    <ProductInfo :produto="livroAtivDiv3" />
    <ProductInfo :produto="livroUrso" />
    <ProductInfo :produto="livroRotina" />
  </section>
</template>

<script>
import {
  livroRotina,
  livroUrso,
  livroAtivDiv,
  livroAtivDiv2,
  livroAtivDiv3,
} from "@/assets/js/livros-sensoriais.js";

export default {
  name: "LivrosSensoriais",
  data() {
    return {
      livroAtivDiv,
      livroAtivDiv2,
      livroAtivDiv3,
      livroUrso,
      livroRotina,
    };
  },
};
</script>



