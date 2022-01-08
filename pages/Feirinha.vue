<template>
  <section class="feirinha" col lg="9">
    <h3 class="box-content text-center">FEIRINHA</h3>
    <PriceSet>
      <div class="box-content">
        <IconArrowRight /><b
          >Valor para 06 itens: R$70,00 / Valor para 12 itens: R$130,00.</b
        ><br />
        <IconArrowRight />Você pode escolher 06 ou 12 itens da quitanda,
        mesclando entre frutas, verduras e legumes.<br />
        <BIconArrowDownCircleFill class="icon-down" animation="throb" /><span
          class="click-text text-center"
          >Clique no nome da fruta abaixo para ver em detalhe.</span
        ><br />
        <div class="fruits-list"> 
          <span
            v-for="fruit in fruitsNames"
            :key="fruit.indexOrig"
            @click="openLightboxOnSlide(fruit.indexOrig)"
            :class="fruit.cor"
            class="m-1"
            >{{ fruit.nome }}</span>
        </div>

        <FsLightbox
          :toggler="toggler"
          :sourceIndex="sourceIndex"
          :sources="images"
        />
      </div>
    </PriceSet>
    <CatalogMasonry :produtos="feirinha" />
    <PriceSet>
      <h5 class="box-content text-center">ITENS FEIRINHA</h5>
    </PriceSet>
    <CatalogMasonry :produtos="itensFeirinha" tipo="cards" />
    <PriceSet>
      <h5 class="box-content text-center">ECOBAGS</h5>
      <p class="box-content">
        <IconArrowRight />
        Tamanho: Largura=24cm x Altura=30cm. <b>Valor: R$15,00</b><br />
        <IconArrowRight />
        Tamanho: Largura=30cm x Altura=35cm. <b>Valor: R$20,00</b><br />
        <IconArrowRight />Pintada à Mão, Em algodão cru, com alça colorida
        (vermelha/verde/laranja) para guardar as frutas/verduras/legumes.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="ecobag" />
  </section>
</template>

<script>
import {
  feirinha,
  itensFeirinha,
  ecobag,
  fruits,
} from "@/assets/js/feirinha.js";
import FsLightbox from "fslightbox-vue";
import { BIcon, BIconArrowDownCircleFill } from "bootstrap-vue";

export default {
  name: "Feirinha",
  components: { FsLightbox, BIcon, BIconArrowDownCircleFill },
  data() {
    return {
      feirinha: feirinha,
      ecobag: ecobag,
      itensFeirinha: itensFeirinha,
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
.feirinha h5 {
  margin-bottom: 10px;
}
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
.click-text {
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



