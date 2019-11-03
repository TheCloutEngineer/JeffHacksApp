<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld />
    <FastFood />
    <AltFood />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import FastFood from "@/components/FastFood.vue";
import AltFood from "@/components/AltFood";
export default {
  name: "home",
  components: {
    AltFood,
    HelloWorld,
    FastFood
  }
};
</script>
