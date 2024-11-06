<template>
    <v-container class="fill-height" fluid>
    <v-row class="justify-center align-center">
        <v-col cols="auto">
        <v-card class="portfolio-card pa-4 d-flex flex-column align-center">

      <v-row class="d-flex justify-center align-center mb-2">
        <span class="text-subtitle-2 text-grey">Total Portfolio</span>
        <v-spacer></v-spacer>
        <v-icon color="green" small>mdi-arrow-up</v-icon>
        <span class="text-success font-weight-bold ml-1">2.36%</span>
      </v-row>
  
      <!-- Main Amount -->
      <v-row class="justify-center">
        <span class="text-h4 font-weight-bold">USD 10,000.00</span>
      </v-row>
  
      <v-divider class="my-4"></v-divider>
  
      <!-- Details (Earnings and Investments) -->
      <v-row class="d-flex justify-center align-center">
        <v-col class="text-center">
          <v-icon color="green" small>mdi-arrow-up</v-icon>
          <span class="text-body-2">Earnings</span>
          <div class="text-h6 font-weight-bold">USD 30,000.00</div>
        </v-col>
  
        <v-divider vertical></v-divider>
  
        <v-col class="text-center">
          <v-icon color="red" small>mdi-arrow-down</v-icon>
          <span class="text-body-2">Investments</span>
          <div class="text-h6 font-weight-bold">USD 20,000.00</div>
        </v-col>
      </v-row>
    </v-card>
        </v-col>
    </v-row>
  </v-container>

</template>
  
  <script>
  export default {
    name: "PortfolioCard",
  };
  </script>
  
  <style scoped>
  .portfolio-card {
    max-width: 320px;
    text-align: center; /* 전체 카드 내의 텍스트를 중앙 정렬 */
  }
  </style>
  