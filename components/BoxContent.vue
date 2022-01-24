<template>
  <component :compType="compType" :is="compType" class="box-content">
    <slot />
  </component>
</template>

<script>
export default {
  name: "BoxContent",
  props: ["compType"],
};
</script>

<style scoped>
.box-content {
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 0.25rem;
  background-color: #fff;
  padding: 1rem;
  width: 100%;
}
h3.box-content,
h5.box-content {
  margin-bottom: 0;
}
p.box-content {
  text-align: center;
  margin-bottom: 0;
}
.bi-arrow-right-circle-fill {
  color: #a92d37;
}

ul {
  padding-left: 0;
  margin-bottom: 0;
}
li {
  text-align: center;
  list-style: none;
}
</style>