<template>
  <section class="livros-sensoriais" col lg="9">
    <h3 class="box-content text-center">LIVROS SENSORIAIS</h3>
    <PriceSet>
      <h5 class="box-content text-center">TEMA ATIVIDADES DIVERSAS</h5>
      <p class="box-content">
        <IconArrowRight /><b>Valor: R$75,00 - Com 4 páginas</b>
      </p>
      <div class="box-content">
         <ul>
          <li>- Página 01 – Bichinho segurando balões</li>
          <li>- Página 02 – Bichinho que escova o dente</li>
          <li>- Página 03 – Formas e encaixe</li>
          <li>- Página 04 – Bichinho que se esconde</li>
          <li>- Dimensões: 21cm x 21cm</li>
        </ul>
      </div>
    </PriceSet>
    <CatalogMasonry :produtos="livroAtivDiv" />
    <PriceSet>
      <h5 class="box-content text-center">TEMA ATIVIDADES DIVERSAS</h5>
      <p class="box-content">
        <IconArrowRight /><b>Valor: R$75,00 - Com 4 páginas</b>
      </p>
      <div class="box-content">
         <ul>
          <li>- Página 01 – Relógio com 2 ponteiros para marcar horas e minutos</li>
          <li>- Página 02 – Ábaco em forma de guarda chuva com contas de 01 a 10</li>
          <li>- Página 03 – Jogo da Velha</li>
          <li>- Página 04 – Árvore de Natal com enfeite de bolinhas</li>
          <li>- Dimensões: 21cm x 21cm</li>
        </ul>
      </div>
    </PriceSet>
    <CatalogMasonry :produtos="livroAtivDiv2" />
    <PriceSet>
      <h5 class="box-content text-center">TEMA ATIVIDADES DIVERSAS</h5>
      <p class="box-content">
        <IconArrowRight /><b>Valor: R$75,00 - Com 4 páginas</b>
      </p>
      <div class="box-content">
         <ul>
          <li>- Página 01 –  Urso que esconde os olhos</li>
          <li>- Página 02 – Ovo com pintinho dentro</li>
          <li>- Página 03 – Boneca(2D) e cama</li>
          <li>- Página 04 – Formas e encaixes</li>
          <li>- Dimensões: 21cm x 21cm</li>
        </ul>
      </div>
    </PriceSet>
    <CatalogMasonry :produtos="livroAtivDiv3" />
    <PriceSet>
      <h5 class="box-content text-center">TEMA URSO</h5>
      <p class="box-content">
        <IconArrowRight /><b>Valor: R$75,00 - Com 4 páginas</b>
      </p>
      <div class="box-content">
         <ul>
          <li>- Página 01 – Urso com balões (letras)</li>
          <li>- Página 02 – Urso que esconde os olhos</li>
          <li>- Página 03 – Quebra-cabeça</li>
          <li>- Página 04 – Urso no rio</li>
          <li>- Dimensões: 21cm x 21cm</li>
        </ul>
      </div>
    </PriceSet>
    <CatalogMasonry :produtos="livroUrso" />
    <PriceSet>
      <h5 class="box-content text-center">TEMA ROTINA</h5>
      <p class="box-content">
        <IconArrowRight /><b>Valor: R$100,00 - Com 6 páginas</b>
      </p>
      <div class="box-content">
         <ul>
          
          <li>- Página 01 – Casa e varal contendo 02 peças de roupa</li>
          <li>- Página 02 – Cozinha</li>
          <li>- Página 03 – Horta</li>
          <li>- Página 04 – Parquinho</li>
          <li>- Página 05 – Banheiro</li>
          <li>- Página 06 – Quarto</li>
          <li>- Dimensões: 21cm x 21cm</li>          
          <li>*Com 01 boneco/a 2D (possível personalizar)</li>
        </ul>
      </div>
    </PriceSet>
    <CatalogMasonry :produtos="livroRotina" />
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
      livroAtivDiv: livroAtivDiv,
      livroAtivDiv2: livroAtivDiv2,
      livroAtivDiv3: livroAtivDiv3,
      livroUrso: livroUrso,
      livroRotina: livroRotina,
    };
  },
};
</script>

<style scoped>
ul {
  padding-left: 0;
  margin-bottom: 0;
}
li {
  list-style: none;
}
</style>

