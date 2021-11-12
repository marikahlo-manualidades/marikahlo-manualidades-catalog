<template>
  <div class="d-flex flex-column main-wrapper">
    <TheHeader @mobile-view-change="updateMobileView($event)" />
    <b-container class="main-container">
      <b-row>
        <div class="content d-flex w-100">
          <b-col v-if="!mobileView" col lg="3"><NavBarSide /></b-col>
          <b-col col lg="9"><Nuxt /></b-col>
        </div>
      </b-row>
    </b-container>
    <TheFooter />
  </div>
</template>

<script>
export default {
  data() {
    return {
      mobileView: false,
    };
  },
  methods: {
    updateMobileView(value) {
      this.mobileView = value;
    },
  },
};
</script>

<style>
.main-wrapper {
  height: 100vh;
}
.main-container {
  flex-basis: 80%;
}
</style>