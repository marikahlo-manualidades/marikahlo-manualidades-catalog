<template>
  <section class="feirinha" col lg="9">
    <h3 class="box-content text-center">FEIRINHA</h3>
    <PriceSet>
      <p class="box-content">
        <IconArrowRight /><b
          >Valor para 06 itens: R$70,00 / Valor para 12 itens: R$130,00.</b
        ><br />
        <IconArrowRight />Você pode escolher 06 ou 12 itens da quitanda, mesclando entre frutas,
        verduras e legumes.<br />
        <span class="verde">Abacate</span>, <span class="amarelo">Abacaxi</span>,
        <span class="laranja">Abóbora</span>, <span class="verde">Alface</span>,
        <span class="amarelo">Banana</span>, <span class="marrom">Batata</span>,
        <span class="roxo">Berinjela</span>,
        <span class="roxo">Beterraba</span>,
        <span class="verde">Brócolis</span>, <span class="laranja">Cacau</span>,
        <span class="amarelo">Caju</span>,
        <span class="verde">Cana de Açúcar</span>,
        <span class="amarelo">Carambola</span>,
        <span class="laranja">Cenoura</span>, <span class="marrom">Coco</span>,
        <span class="verde">Kiwi</span>, <span class="laranja">Laranja</span>,
        <span class="vermelho">Maçã</span>, <span class="laranja">Mamão</span>,
        <span class="amarelo">Manga</span>, <span class="verde">Melancia</span>,
        <span class="amarelo">Milho</span>, <span class="vermelho">Morango</span>,
        <span class="vermelho">Rabanete</span>,
        <span class="vermelho">Tomate</span>, <span class="roxo">Uva</span>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="feirinha" />
    <PriceSet>
      <h5 class="box-content text-center">ITENS FEIRINHA</h5>
    </PriceSet>
    <CatalogMasonry :produtos="itensFeirinha" tipo="cards"/>
    <PriceSet>
      <h5 class="box-content text-center">ECOBAGS</h5>
      <p class="box-content">
        <IconArrowRight />
        Tamanho: Largura=24cm x Altura=30cm. <b>Valor: R$15,00</b><br />
        <IconArrowRight />
        Tamanho: Largura=30cm x Altura=35cm. <b>Valor: R$20,00</b><br />
        <IconArrowRight />Pintada à Mão, Em algodão cru, com alça colorida (vermelha/verde/laranja) para guardar as frutas/verduras/legumes.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="ecobag" />
  </section>
</template>

<script>
import { feirinha, itensFeirinha, ecobag } from "@/assets/js/feirinha.js";

export default {
  name: "Feirinha",
  data() {
    return {
      feirinha: feirinha,
      ecobag: ecobag,
      itensFeirinha: itensFeirinha
    };
  },
};
</script>

<style scoped>
.feirinha h5 {
  margin-bottom: 10px;
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
</style>



