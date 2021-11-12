<template>
  <b-card
    :title="produto.titulo"
    :img-src="produto.imagem"
    img-alt="Image"
    @click="toggler = !toggler"
  >
    <b-card-text>
      {{ produto.descricao }}
    </b-card-text>
    <hr v-if="produto.preco" />
    <div class="card-preco" v-if="produto.preco">
      <span>{{ produto.preco }}</span>
    </div>
    <FsLightbox :toggler="toggler" :sources="[produto.imagem]" />
  </b-card>
</template>

<script>
import FsLightbox from "fslightbox-vue";
export default {
  name: "Card",
  components: { FsLightbox },
  props: {
    produto: Object,
  },
  data() {
    return {
      toggler: false,
    };
  },
};
</script>

<style scoped>
hr {
  margin: 0.1rem;
}
.card {
  margin: 0 0 1em;
  padding: 0.25rem;
}
.card:hover {
  box-shadow: 0 0 1em rgba(0, 0, 0, 0.6);
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
.card-preco {
  margin-top: 10px;
}
.card-preco span {
  font-weight: 700;
}
</style>