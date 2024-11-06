<template>
<v-expansion-panels class="pa-4 rounded-panels bg-white"  variant="popout">
    <v-container class="fill-height" fluid>
    <v-row class="justify-center align-center">
        <v-card class="pa-4" outlined>
    <v-card-title>
      Total Savings
      <v-spacer></v-spacer>
      <v-chip color="green lighten-4" text-color="green darken-1" class="ml-2">
        <v-icon left>mdi-arrow-up</v-icon>
        2.36%
      </v-chip>
    </v-card-title>
    <v-card-subtitle class="text-h5 font-weight-bold">
      USD 5,000.00
    </v-card-subtitle>
    <v-card-text class="d-flex align-center">
      <v-container class="pa-0">
        <v-row class="fill-height align-center">
          <v-col v-for="(bar, index) in bars" :key="index" class="px-1">
            <div
              class="bar"
              :style="{ height: bar + '%', backgroundColor: '#E0E0E0', borderRadius: '4px' }"
            ></div>
          </v-col>
        </v-row>
      </v-container>
    </v-card-text>
  </v-card>
    </v-row>
  </v-container>
</v-expansion-panels>
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
  