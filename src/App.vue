<template>
  <v-app>
    <v-main>
      <HelloWorld/>
      <FooterMenu/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FooterMenu from './components/FooterMenu.vue';

export default {
  name: 'App',

  components: {
    HelloWorld,
    FooterMenu,
  },

  data: () => ({
    //
  }),
}
</script>
