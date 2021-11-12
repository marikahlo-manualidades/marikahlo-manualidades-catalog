<template>
  <section class="brinquedos-diversos" col lg="9">
    <h3 class="box-content text-center">BRINQUEDOS DIVERSOS</h3>
    <PriceSet>
      <h5 class="box-content text-center">DEDOCHES</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$25,00 => 4 unidades</b>
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="dedoches" />
    <PriceSet>
      <h5 class="box-content text-center">JOGO DA MEMÓRIA</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$30,00</b><br />
        <IconArrowRight />Contendo 06 pares de peças (animais). Cada peça mede
        cerca de 6cmx4cm – total de 12 peças.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="jogomemoria" />
    <PriceSet>
      <h5 class="box-content text-center">JOGO DA VELHA</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$40,00</b><br />
        <IconArrowRight />Tabuleiro com cerca de 15cm x 15cm
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="jogovelha" />
    <PriceSet>
      <h5 class="box-content text-center">JOGO DE ENCAIXE COM PINO CENTRAL</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$40,00</b><br />
        <IconArrowRight />Altura de cerca de 18cm
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="jogoencaixe" />
    <PriceSet>
      <h5 class="box-content text-center">ÁBACO</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$35,00</b><br />
        <IconArrowRight />Tamanho A4
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="abaco" />
    <PriceSet>
      <h5 class="box-content text-center">PEIXINHOS COM IMÃ E VARA DE PESCAR</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor unitário: R$4,00</b> – Quantidade mínima para
        pedido: 6 unidades.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="peixinhos" />
    <PriceSet>
      <h5 class="box-content text-center">ALMOFADA ÁFRICA LETRA</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$50,00</b><br>
        <IconArrowRight />Fazemos a letra e o bichinho conforme a escolha 
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="almofadaafrica" />
    <PriceSet>
      <h5 class="box-content text-center">PORTA COPOS</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$25,00</b><br>
        <IconArrowRight />06 unidades - Frutas: Laranja, Melancia, Kiwi, Limão, Morango e Maçã
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="portacopos" />
    <PriceSet>
      <h5 class="box-content text-center">SANDUÍCHE</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$40,00</b><br>
        <IconArrowRight />Sanduiche de pão de forma com salada de alface americana, tomate, queijo suíço e hambúrguer de carne bovina + um saquinho para o sanduíche.
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="sanduiche" />
    <PriceSet>
      <h5 class="box-content text-center">PANELA</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$25,00</b><br>
        <IconArrowRight />01 Panela Com Cabo e Tampa
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="panela" />
    <PriceSet>
      <h5 class="box-content text-center">TURMA DA GALINHA PINTADINHA</h5>
      <p class="box-content">
        <IconArrowRight />
        <b>Valor: R$120,00</b><br>
        <IconArrowRight />Galinha Pintadinha, Galo Carijó e Pintinho Amarelinho 
      </p>
    </PriceSet>
    <CatalogMasonry :produtos="galinhapintadinha" />
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
  sanduiche

} from "@/assets/js/brinquedos-diversos.js";
export default {
  name: "BrinquedosDiversos",
  data() {
    return {
      dedoches: dedoches,
      jogomemoria: jogomemoria,
      jogovelha: jogovelha,
      jogoencaixe: jogoencaixe,
      peixinhos: peixinhos,
      galinhapintadinha: galinhapintadinha,
      almofadaafrica: almofadaafrica,
      abaco: abaco,
      portacopos: portacopos,
      panela: panela,
      sanduiche: sanduiche

    };
  },
};
</script>