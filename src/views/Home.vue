<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld />
    <FastFood />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import FastFood from "@/components/FastFood.vue";
export default {
  name: "home",
  components: {
    HelloWorld,
    FastFood
  }
};
</script>
