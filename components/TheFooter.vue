<template>
  <footer>
    <span class="mr-2 mt-1">mari</span
    ><img class="mb-1" src="~/assets/image/mari-kahlo-logo.png" /><span
      class="ml-2 mt-1"
    >
      kahlo</span
    >
  </footer>
</template>

<script>
export default {
  name: "TheFooter",
};
</script>

<style scoped>
footer {
  display: flex;
  justify-content: center;
  align-items: center;
  background: -webkit-linear-gradient(to right, #a92d37, #fff, #7a8f10);
  background: linear-gradient(to right, #a92d37, #fff, #7a8f10);
  margin-top: 1rem;
  border-top: 1px solid rgba(0, 0, 0, 0.125);
}
footer span {
  font-size: 1.5rem;
  letter-spacing: 0.1rem;
}
footer img {
  height: 2.5rem;
  filter: drop-shadow(2px 2px 2px rgb(0, 0, 0, 0.9));
}
</style>