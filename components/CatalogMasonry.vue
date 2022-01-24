<template>
  <masonry class="masonry mt-2" :cols="{ default: 3, 992: 2, 576: 1 }" :gutter="30">
    <div v-for="(produto, index) in produtos" :key="index">
      <CardFSLightBox v-if="produto.titulo" :produto="produto" />
      <VideoWrapper
        v-else-if="produto.imagem.endsWith('mp4')"
        :vdsrc="produto.imagem"
        :postersrc="produto.poster"
        @click.native="openLightboxOnSlide(index)"
      />
      <ImageWrapper
        v-else
        @click.native="openLightboxOnSlide(index)"
        :imgsource="produto.imagem"
      />
    </div>
    <FsLightbox
      v-if="tipo === 'imagens'"
      :toggler="toggler"
      :sourceIndex="sourceIndex"
      :sources="images"
    />
  </masonry>
</template>

<script>
import Vue from "vue";
import VueMasonry from "vue-masonry-css";
import FsLightbox from "fslightbox-vue";

Vue.use(VueMasonry);
export default {
  name: "CatalogMasonry",
  components: { FsLightbox },
  props: {
    produtos: Array,
    tipo: {
      type: String,
      default: "imagens",
    },
  },
  data() {
    return {
      toggler: false,
      sourceIndex: 0,
    };
  },
  computed: {
    images() {
      return this.produtos.map((produto) => produto.imagem);
    },
  },
  methods: {
    openLightboxOnSlide(number) {
      this.sourceIndex = number;
      this.toggler = !this.toggler;
      // document.querySelectorAll('video').forEach(video => {
      //   video.pause()})
    },

  },
};
</script>

