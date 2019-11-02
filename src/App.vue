<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Team #16 </span>
        <span class="font-weight-light">T8sty</span>
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
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data: () => ({
    //
  })
};
</script>
