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
  
  <style scoped>
  .footer-custom {
    position: fixed; /* 화면 하단에 고정 */
    bottom: 0; /* 화면 맨 아래에 위치 */
    left: 0;
    width: 100%; /* 전체 너비 */
    background-color: #0046FF;
    text-align: center;
    display: flex;
    flex-direction: column;
    z-index: 999; /* 다른 요소들 위에 표시되도록 설정 */
  }
  </style>
  