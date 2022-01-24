<template>
  <div class="d-flex justify-content-center flex-wrap">
    <BoxContent v-if="produto.titulo" compType="h5" class="text-center">{{
      produto.titulo
    }}</BoxContent>
    <BoxContent compType="p" v-if="produto.valor"
      ><span
        ><IconArrowRight /> <b>{{ produto.valor }}</b
        ><br
      /></span>
      <span v-for="(desc, index) in produto.descricao" :key="index"
        ><IconArrowRight />{{ desc }}<br
      /></span>
      <slot name="frutas"></slot>
    </BoxContent>
    <BoxContent v-if="produto.paginas" compType="div">
      <ul>
        <li v-for="(pagina, index) in produto.paginas" :key="index">
          <b-icon icon="book" class="mr-1 bi-icon-book"></b-icon>{{ pagina }}
        </li>
      </ul>
    </BoxContent>
    <CatalogMasonry :produtos="produto.imagens" :tipo="tipo" />
  </div>
</template>

<script>
import { BIcon, BIconBook } from "bootstrap-vue";
export default {
  name: "ProductInfo",
  components: { BIcon, BIconBook },
  props: ["produto", "tipo"],
};
</script>

<style scoped>
.bi-icon-book {
  color: #7a8f10;
}
</style>