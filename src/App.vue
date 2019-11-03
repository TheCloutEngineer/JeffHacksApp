<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="align-center headline text-uppercase">
        <span>Team #16 </span>
        <span class="font-weight-light">T8sty App</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/Ksaboor/JeffHacksApp"
        target="_blank"
      >
        <span class="mr-2">GitHub</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <HelloWorld />
      <FastFood />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import FastFood from "./components/FastFood";
export default {
  name: "App",
  components: {
    HelloWorld,
    FastFood
  },
  data: () => ({
    //
  })
};
</script>
