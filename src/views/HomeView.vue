<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Bienvenido a tu aplicación Vue.js"/>
    <!-- Enlace a la lista de problemas -->
    <router-link to="/issue-list">Ir a la lista de problemas</router-link>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
