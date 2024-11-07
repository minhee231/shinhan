<template>
    <v-footer class="footer-custom text-center d-flex flex-column">
      <div>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          :icon="icon"
          class="mx-5"
          variant="text"
          color="white"
        ></v-btn>
      </div>
    </v-footer>
  </template>
  
<script>
    export default {
      data: () => ({
        icons: ['mdi-home', 'mdi-share', 'mdi-credit-card-outline', 'mdi-chart-line'],
      }),
    }
  </script>
  
  <style scoped>
  .footer-custom {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #0046FF;
    text-align: center;
    display: flex;
    flex-direction: column;
    z-index: 999;
  }
  </style>
  