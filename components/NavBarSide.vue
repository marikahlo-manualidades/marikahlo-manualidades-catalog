<template>
  <div>
    <span class="d-inline-block w-100 text-center">CATEGORIAS</span>
    <hr />
    <b-nav vertical class="w-100">
      <li><NuxtLink to="/">Início</NuxtLink></li>
      <li><NuxtLink to="/calendarios">Calendários</NuxtLink></li>
      <li><NuxtLink to="/feirinha" >Feirinha</NuxtLink></li>
      <li><NuxtLink to="/quadrosrotina">Quadros de Rotina</NuxtLink></li>
      <li><NuxtLink to="/kitfesta">Kit Festa</NuxtLink></li>
      <li><NuxtLink to="/guirlandasmobiles">Guirlandas e Móbiles</NuxtLink></li>
      <li><NuxtLink to="/livrossensoriais">Livros Sensoriais</NuxtLink></li>
      <li><NuxtLink to="/enfeitesnatalinos">Enfeites Natalinos</NuxtLink></li>
      <li><NuxtLink to="/brinquedosdiversos">Brinquedos Diversos</NuxtLink></li>
    </b-nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
hr {
  margin-top: 0.3rem;
}
div {
  background-color: #fff;
  box-shadow: 0 0 1em rgba(0, 0, 0, 0.1);
  margin-top: 10px;
}
div span {
  font-size: 1.5rem;
  font-weight: 700;
  margin-top: 0.25rem;
}
div li a {
  display: block;
  color: #7a8f10;
  padding: 0.5rem 1rem;
  text-decoration: none;
  letter-spacing: 0.05rem;
}
div li a:hover {
  background-color: #e6787f;
  font-weight: 700;
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