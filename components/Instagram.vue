<template>
  <a
    href="https://www.instagram.com/marikahlo.manualidades"
    target="_blank"
    rel="noopener noreferrer"
  >
    <b-icon icon="instagram" font-scale="2" class="ml-3 instagram"></b-icon
  ></a>
</template>

<script>
import { BIcon, BIconInstagram } from "bootstrap-vue";
export default {
  name: "Instagram",
  components: {
    BIcon,
    BIconInstagram,
  },
};
</script>

<style scoped>
.instagram {
  background: #833ab4; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to top right,
    #fcb045,
    #fd1d1d,
    #833ab4
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to top right,
    #fcb045 20%,
    #fd1d1d,
    #833ab4 80%
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  color: #fff;
  border-radius: 20px;
  animation: pulse 1s infinite;
  -webkit-filter: drop-shadow(2px 2px 2px rgb(0, 0, 0, 0.8));
  filter: drop-shadow(2px 2px 2px rgb(0, 0, 0, 0.8));
}
@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}
</style>