<template>
  <footer>
    <span class="mr-2 mt-1">MARI </span><img class="mb-1" src="~/assets/image/mari-kahlo-logo.png"><span class="ml-2 mt-1"> KAHLO</span>
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
  background: -webkit-linear-gradient(to right,#7a8f10, #fff, #a92d37);
  background: linear-gradient(to right, #7a8f10, #fff, #a92d37); 
  margin-top: 1rem;
  border-top: 1px solid rgba(50, 50, 50, 0.1);
  
}
footer span {
    font-family: 'patterns__dotsregular';
    filter: drop-shadow(2px 2px 2px rgb(0, 0, 0, 0.8));
}
footer img {
    height: 2.5rem;
    filter: drop-shadow(2px 2px 2px rgb(0, 0, 0, 0.9));
}
</style>