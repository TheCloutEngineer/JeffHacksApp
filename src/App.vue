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
      <AltFood />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import FastFood from "./components/FastFood";
import AltFood from "./components/AltFood";
export default {
  name: "App",
  components: {
    AltFood,
    HelloWorld,
    FastFood
  },
  data: () => ({
    //
  })
};
</script>
