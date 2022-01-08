<template>
  <section class="feirinha" col lg="9">
    <h3 class="box-content text-center">FEIRINHA</h3>
    <PriceSet>
      <p class="box-content">
        <IconArrowRight /><b
          >Valor para 06 itens: R$70,00 / Valor para 12 itens: R$130,00.</b
        ><br />
        <IconArrowRight />Você pode escolher 06 ou 12 itens da quitanda,
        mesclando entre frutas, verduras e legumes.<br />
        <BIconArrowDownCircleFill class="icon-down" animation="throb" /><span
          class="click-text text-center"
          >Clique no nome da fruta abaixo para ver em detalhe.</span
        ><br />
        <span class="verde m-3" @click="openLightboxOnSlide(0)">Abacate</span>
        <span class="amarelo m-3" @click="openLightboxOnSlide(1)">Abacaxi</span>
        <span class="laranja m-3" @click="openLightboxOnSlide(2)">Abóbora</span>
        <span class="verde m-3" @click="openLightboxOnSlide(3)">Alface</span>
        <span class="amarelo m-3" @click="openLightboxOnSlide(5)">Banana</span>
        <span class="marrom m-3" @click="openLightboxOnSlide(7)">Batata</span>
        <span class="roxo m-3" @click="openLightboxOnSlide(8)">Berinjela</span>
        <span class="roxo m-3" @click="openLightboxOnSlide(9)">Beterraba</span>
        <span class="verde m-3" @click="openLightboxOnSlide(10)">Brócolis</span>
        <span class="laranja m-3" @click="openLightboxOnSlide(11)">Cacau</span>
        <span class="amarelo m-3" @click="openLightboxOnSlide(13)">Caju</span>
        <span class="verde m-3" @click="openLightboxOnSlide(14)"
          >Cana de Açúcar</span
        >
        <span class="amarelo m-3" @click="openLightboxOnSlide(15)"
          >Carambola</span
        >
        <span class="laranja m-3" @click="openLightboxOnSlide(16)"
          >Cenoura</span
        >
        <span class="marrom m-3" @click="openLightboxOnSlide(17)">Coco</span>
        <span class="verde m-3" @click="openLightboxOnSlide(19)">Kiwi</span>
        <span class="laranja m-3" @click="openLightboxOnSlide(20)"
          >Laranja</span
        >
        <span class="vermelho m-3" @click="openLightboxOnSlide(21)">Maçã</span>
        <span class="laranja m-3" @click="openLightboxOnSlide(22)">Mamão</span>
        <span class="amarelo m-3" @click="openLightboxOnSlide(23)">Manga</span>
        <span class="verde m-3" @click="openLightboxOnSlide(24)">Melancia</span>
        <span class="amarelo m-3" @click="openLightboxOnSlide(25)">Milho</span>
        <span class="vermelho m-3">Morango</span>
        <span class="vermelho m-3" @click="openLightboxOnSlide(27)"
          >Rabanete</span
        >
        <span class="vermelho m-3" @click="openLightboxOnSlide(28)"
          >Tomate</span
        >
        <span class="roxo m-3" @click="openLightboxOnSlide(29)">Uva</span>
        <FsLightbox
          :toggler="toggler"
          :sourceIndex="sourceIndex"
          :sources="images"
        />
      </p>
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
  },
  methods: {
    openLightboxOnSlide(number) {
      this.sourceIndex = number;
      this.toggler = !this.toggler;
    },
  },
};
</script>

<style scoped>
.feirinha h5 {
  margin-bottom: 10px;
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



