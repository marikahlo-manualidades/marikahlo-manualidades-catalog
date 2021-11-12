<template>
  <aside v-on-clickaway="away">
    <span class="categories d-inline-block w-100 text-center font-weight-bold"
      >CATEGORIAS</span
    >
    <hr />
    <b-nav vertical class="w-100">
          <b-nav vertical class="w-100">
      <li><NuxtLink @click.native="hideMenu" to="/">Início</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/Calendarios">Calendários</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/Feirinha">Feirinha</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/Chaveiros">Chaveiros</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/KitFesta">Kit Festa</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/Mobiles">Móbiles</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/LivrosSensoriais">Livros Sensoriais</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/EnfeitesNatalinos">Enfeites Natalinos</NuxtLink></li>
      <li><NuxtLink @click.native="hideMenu" to="/BrinquedosDiversos">Brinquedos Diversos</NuxtLink></li>
    </b-nav>
    </b-nav>
  </aside>
</template>

<script>
import { mixin as clickaway } from 'vue-clickaway';
export default {
  name: "NavBarMobile",
  mixins: [ clickaway ],
  emits: ['hideMenu'],
  methods: {
    hideMenu() {
      this.$emit('hide-menu')
    },
    away: function() {
      this.hideMenu();
    },
  },
};
</script>

<style scoped>
aside {
  position: absolute;
  top: 100px;
  transform: translateY(25px);
  width: 80%;
  max-width: 400px;
  z-index: 1000;
  box-shadow: 0 0 1em rgba(0, 0, 0, 0.8);
  background-color: #fff;
}
aside span {
  font-size: 1.5rem;
  background-color: #fff;
  margin-top: 0.25rem;
}
hr {
  margin-top: 0.3rem;
}

aside li a {
  display: block;
  color: #7a8f10;
  padding: 0.5rem 1rem;
  text-decoration: none;
}
aside li a:hover {
  background-color: #e6787f;
  color: #fff;
}
.nuxt-link-active {
  font-weight: 700;
}
a.nuxt-link-exact-active {
  color: #fff;
  background-color: #a92d37;
}
</style>