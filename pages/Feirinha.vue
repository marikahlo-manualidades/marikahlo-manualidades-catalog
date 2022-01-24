<template>
  <section class="feirinha" col lg="9">
    <BoxContent compType="h3" class="text-center">FEIRINHA</BoxContent>
    <ProductInfo :produto="feirinha">
      <template #frutas>
        <BIconArrowDownCircleFill class="icon-down" animation="throb" /><span
          class="hortalica-text text-center"
          >Clique no nome da hortaliça abaixo para ver em detalhe.</span
        ><br />
        <div class="fruits-list">
          <span
            v-for="fruit in fruitsNames"
            :key="fruit.indexOrig"
            @click="openLightboxOnSlide(fruit.indexOrig)"
            :class="fruit.cor"
            class="m-1"
            >{{ fruit.nome }}</span
          >
        </div>

        <FsLightbox
          :toggler="toggler"
          :sourceIndex="sourceIndex"
          :sources="images"
        />
      </template>
    </ProductInfo>
    <ProductInfo :produto="itensFeirinha" tipo="cards" />
    <ProductInfo :produto="ecobags" />
  </section>
</template>

<script>
import {
  feirinha,
  itensFeirinha,
  ecobags,
  fruits,
} from "@/assets/js/feirinha.js";
import FsLightbox from "fslightbox-vue";
import { BIcon, BIconArrowDownCircleFill } from "bootstrap-vue";
import ProductInfo from "../components/ProductInfo.vue";

export default {
  name: "Feirinha",
  components: { FsLightbox, BIcon, BIconArrowDownCircleFill, ProductInfo },
  data() {
    return {
      feirinha,
      ecobags,
      itensFeirinha,
      toggler: false,
      sourceIndex: 0,
      sources: this.images,
    };
  },
  computed: {
    images() {
      return fruits.map((fruit) => fruit.imagem);
    },
    fruitsNames() {
      const fruitsWithIndex = fruits.map((fruit, index) => {
        return { ...fruit, indexOrig: index };
      });
      return fruitsWithIndex.filter((fruit) => fruit.nome);
    },
  },
  methods: {
    openLightboxOnSlide(number) {
      this.sourceIndex = number;
      this.toggler = !this.toggler;
    },
    getIndexOfFruit() {},
  },
};
</script>

<style scoped>
.fruits-list {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin-bottom: 0 !important;
}
.amarelo,
.laranja,
.roxo,
.verde,
.marrom,
.vermelho {
  font-size: 1.25rem;
  padding: 0 0.5rem;
}
.amarelo:hover,
.laranja:hover,
.roxo:hover,
.verde:hover,
.marrom:hover,
.vermelho:hover {
  cursor: pointer;
  background-color: rgb(240, 240, 240);
}
.hortalica-text {
  font-weight: bolder;
  text-decoration: underline;
  font-size: 1.1rem;
}
.verde {
  color: #009100;
}
.laranja {
  color: #ff642b;
}
.roxo {
  color: #663399;
}
.vermelho {
  color: #ff0000;
}
.amarelo {
  color: #f1ad01;
}
.marrom {
  color: #b67a5e;
}
.bi-arrow-down-circle-fill {
  color: #a92d37;
  margin: 0 1rem;
}
</style>



