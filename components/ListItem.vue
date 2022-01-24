<template>
  <b-list-group-item class="d-flex justify-content-start align-items-center">
    <IconArrowRight />
    <slot></slot>
  </b-list-group-item>
</template>

<script>
import { BIcon, BIconArrowRightCircleFill } from "bootstrap-vue";
export default {
  components: {
    BIcon,
    BIconArrowRightCircleFill,
  },
    name: "ListItem"
};
</script>

<style>
.bi-arrow-right-circle-fill {
  color: #a92d37;
}
.list-group-item {
  padding: 0.5rem 1rem;
}
</style>