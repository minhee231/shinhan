<template>
    <v-footer class="footer-custom text-center d-flex flex-column">
      <div>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          :icon="icon"
          class="mx-4"
          variant="text"
          color="white"
        ></v-btn>
      </div>
    </v-footer>
  </template>
  
  <script>
    export default {
      data: () => ({
        icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram'],
      }),
    }
  </script>
  

<style>

.footer-custom {
  background-color: #0046FF;
  text-align: center;
  display: flex;
  flex-direction: column;
}

</style>