<template>
  <div class="d-flex justify-content-center flex-wrap">
     <slot></slot>
  </div>
</template>

<script>
export default {
    name: 'PriceSet',
};
</script>

<style scoped>
.bi-arrow-right-circle-fill {
  color: #a92d37;
}
p {
 margin-bottom: 0;
 text-align: center;
}
p:last-child {
  margin-bottom: 10px;
}
div {
  text-align: center;
}
div:last-child {
  margin-bottom: 10px;
}
h3, h5{
  margin-bottom: 0;
  margin-top: 10px;
}
</style>