<template>
  <section class="brinquedos-diversos" col lg="9">
    <BoxContent compType="h3" class="text-center mb-2"
      >BRINQUEDOS DIVERSOS</BoxContent
    >
    <ProductInfo :produto="dedoches" />
    <ProductInfo :produto="jogomemoria" />
    <ProductInfo :produto="jogovelha" />
    <ProductInfo :produto="bolinhas" />
    <ProductInfo :produto="jogoencaixe" />
    <ProductInfo :produto="abaco" />
    <ProductInfo :produto="peixinhos" />
    <ProductInfo :produto="almofadaafrica" />
    <ProductInfo :produto="portacopos" />
    <ProductInfo :produto="sanduiche" />
    <ProductInfo :produto="panela" />
    <ProductInfo :produto="galinhapintadinha" />
  </section>
</template>

<script>
import {
  dedoches,
  jogomemoria,
  jogovelha,
  jogoencaixe,
  peixinhos,
  galinhapintadinha,
  almofadaafrica,
  abaco,
  portacopos,
  panela,
  sanduiche,
  bolinhas,
} from "@/assets/js/brinquedos-diversos.js";

export default {
  name: "BrinquedosDiversos",
  data() {
    return {
      dedoches,
      jogomemoria,
      jogovelha,
      jogoencaixe,
      peixinhos,
      galinhapintadinha,
      almofadaafrica,
      abaco,
      portacopos,
      panela,
      sanduiche,
      bolinhas,
    };
  },
};
</script>