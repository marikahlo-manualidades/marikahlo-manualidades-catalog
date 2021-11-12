<template>
  <img class="img-fluid img-thumbnail" :src="imgsource"/>
</template>

<script>
export default {
  name: "ImageWrapper",
  props: {
    imgsource: String,
  },
};
</script>

<style scoped>
img {
  margin-bottom: 1em;
}
img:hover {
  box-shadow: 0 0 1em rgba(0, 0, 0, 0.6);
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
</style>