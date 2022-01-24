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
  border-radius: 3px;
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
  border: 1px solid #00910044; 
  color: #009100;
}
.verde:hover {
  background-color: #009100;
  color: #fff
}
.laranja {
  border: 1px solid #ff642b44; 
  color: #ff642b;
}
.laranja:hover {
  background-color: #ff642b;
  color: #fff
}
.roxo {
  border: 1px solid #66339944; 
  color: #663399;
}
.roxo:hover {
  background-color: #663399;
  color: #fff
}
.vermelho {
  border: 1px solid #ff000044; 
  color: #ff0000;
}
.vermelho:hover {
  background-color: #ff0000;
  color: #fff
}
.amarelo {
  border: 1px solid #f1ad0155; 
  color: #f1ad01;
}
.amarelo:hover {
  background-color: #f1ad01;
  color: #fff
}
.marrom {
  border: 1px solid #b67a5e44; 
  color: #b67a5e;
}
.marrom:hover {
  background-color: #b67a5e;
  color: #fff
}
.bi-arrow-down-circle-fill {
  color: #a92d37;
  margin: 0 1rem;
}
</style>



