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
  background: -webkit-linear-gradient(to right, #ce7e86, #fff, #acb96b);
  background: linear-gradient(to right, #ce7e86, rgb(255, 255, 255), #acb96b);
  margin-top: 1rem;
  border-top: 1px solid rgba(0, 0, 0, 0.125);
}
footer span {
  font-size: 1.5rem;
  letter-spacing: 0.1rem;
}
footer img {
  height: 2.5rem;
  filter: drop-shadow(0px 0px 3px rgb(0, 0, 0, 0.9));
  -webkit-filter: drop-shadow(0px 0px 3px rgb(0, 0, 0, 0.9));
}
</style>