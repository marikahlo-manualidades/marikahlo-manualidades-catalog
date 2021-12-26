<template>
  <header class="header" :class="{'fixed-header': mobileView}">
    <div class="d-flex align-items-center">
      <b-icon
        v-if="mobileView"
        icon="list"
        font-scale="2.5"
        @click="showNavChange"
      ></b-icon>
      <transition name="fade">
        <NavBarMobile v-if="showNav" @hide-menu="showNav = false" :scY="scY"/>
      </transition>

      <div class="logo-wrapper w-100 d-flex justify-content-center align-items-center">
        <NuxtLink
          to="/"
          class="d-flex flex-column align-items-center justify-content-center"
          :class="{'mb-1': scY > 299}"
        >
          <b-img
            v-bind="mainProps"
            src="~/assets/image/mari-kahlo-logo.png"
            alt="MARI KAHLO LOGO"
          ></b-img>
          <span  v-if="scY < 300">mari kahlo</span>
          </NuxtLink
        >
      </div>
    </div>
  </header>
</template>

<script>
import { BIcon, BIconList } from "bootstrap-vue";
export default {
  name: 'TheHeader',
  components: {
    BIcon,
    BIconList,
  },
  props: ['scY'],
  data() {
    return {
      mainProps: { width: 178, height: 80 },
      mobileView: false,
      showNav: false,
    };
  },
  methods: {
    handleView() {
      this.mobileView = window.innerWidth < 992;
      if (window.innerWidth > 992 && this.showNav === true)
        this.showNav = false;
    },
    showNavChange() {
      this.showNav = !this.showNav;
    },
  },
  watch: {
    mobileView(value) {
      this.$emit("mobile-view-change", value);
    },
  },
  mounted() {
    this.handleView();
    window.addEventListener("resize", this.handleView);
  },
};
</script>

<style scoped>
header {
  margin: 0;
  background: -webkit-linear-gradient(to right, #7a8f10, #fff, #a92d37);
  background: linear-gradient(to right, #7a8f10, rgb(255, 255, 255), #a92d37);
  border-bottom: 1px solid rgba(0, 0, 0, 0.125);
}
header a {
  color: #000;
  text-decoration: none;
}
span {
  font-size: 1.9rem;
  letter-spacing: 0.1rem;
  font-weight: 500;
  margin: -5px;
}
svg {
  position: absolute;
  margin-left: 1.5rem;
  background-color: rgb(169, 45, 55);
  color: #fff;
  padding: 5px;
  border-radius: 10px;
  box-shadow: 0 0 0.15em rgba(0, 0, 0, 0.8);
}
svg:hover {
  cursor: pointer;
}
.fixed-header {
  position: fixed;
  top: 0;
  z-index: 9999;
  min-width: 100vw;
}

.logo-wrapper img {
  filter: drop-shadow(2px 2px 2px rgb(0, 0, 0, 0.9));
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>