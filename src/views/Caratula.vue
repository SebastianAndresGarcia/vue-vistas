<template>

  <div class="home">
    <top-nav-bar></top-nav-bar>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>

  </div>

</template>

<script lang="ts">
import Vue from 'vue';
import NavBarTop from "@/components/NavBarTop.vue";

export default Vue.extend({
  name: 'caratula-1',

  data: () => ({
    //
  }),
  components: {
    "top-nav-bar": NavBarTop,
    
  }
});

</script>