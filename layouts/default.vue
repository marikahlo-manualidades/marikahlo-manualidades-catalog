<template>
  <div class="d-flex flex-column main-wrapper">
    <TheHeader @mobile-view-change="updateMobileView($event)" :scY="scY"/>
    <b-container
      class="main-container"
      :class="{ 'fixed-header-margin': mobileView }"
    >
      <b-row>
        <div class="content d-flex w-100" v-if="isLoading">
          <b-col v-if="!mobileView" col lg="3"><NavBarSide /></b-col>
          <b-col col lg="9"><Nuxt /></b-col>
        </div>
        <div class="spinner w-100" v-else>
          <b-col col lg="12"><BaseSpinner /></b-col>
        </div>
      </b-row>
    </b-container>
    <transition name="fade">
      <div id="pagetop" class="pagetop" v-show="scY > 300" @click="toTop">
        <b-icon icon="arrow-up-circle-fill" class="h1"></b-icon>
      </div>
    </transition>
    <TheFooter />
  </div>
</template>

<script>
import { BIcon, BIconArrowUpCircleFill } from "bootstrap-vue";
export default {
  components: {
    BIcon,
    BIconArrowUpCircleFill,
  },
  data() {
    return {
      mobileView: false,
      isLoading: false,
      scTimer: 0,
      scY: 0,
    };
  },
  methods: {
    updateMobileView(value) {
      this.mobileView = value;
    },
    handleScroll: function () {
      if (this.scTimer) return;
      this.scTimer = setTimeout(() => {
        this.scY = window.scrollY;
        clearTimeout(this.scTimer);
        this.scTimer = 0;
      }, 100);
    },
    toTop: function () {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
  mounted() {
    this.isLoading = true;
    window.addEventListener("scroll", this.handleScroll);
  },
};
</script>

<style>
.main-wrapper {
  height: 100vh;
}
.main-container {
  flex: 1;
}
.fixed-header-margin {
  margin-top: 125px;
}
.pagetop {
  position: -webkit-sticky;
  position: sticky;
  bottom: 0;
  margin-left: auto; 
  margin-right: 10px;
}
.bi-arrow-up-circle-fill {
  color: #a92d37;
}
.bi-arrow-up-circle-fill:hover {
  color: #e6787f;
}

.fade-enter-active, .fade-leave-active {
  -webkit-transition: opacity .5s ease;
  transition: opacity .5s ease;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>