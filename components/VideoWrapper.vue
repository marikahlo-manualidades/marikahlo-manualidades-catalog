<template>
  <video class="img-fluid img-thumbnail" :src="vdsrc" :poster="postersrc"/>
</template>

<script>
export default {
    name: 'VideoWrapper',
    props: {
        vdsrc: String,
        postersrc: String
    }    
}
</script>

<style scoped>
video {
  margin-bottom: 1em;
}
video:hover {
  box-shadow: 0 0 1em rgba(0, 0, 0, 0.6);
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
</style>