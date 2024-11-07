<template>
<v-expansion-panels class="pa-4 rounded-panels bg-white"  variant="popout">
    <v-container class="fill-height" fluid>
    <v-row class="justify-center align-center ">
    <v-card class="pa-4 container-custom portfolio-card rounded-xl" outlined>
    <v-card-title>
        <span class="text-subtitle-1 font-weight-bold  text-white">자산</span>
      <v-spacer></v-spacer>
      
    </v-card-title>
    <!-- <v-card-subtitle class="text-h5 font-weight-bold text-white" style="color: white;">
      USD 5,000.00
    </v-card-subtitle> -->
        <v-col class="text-center">
            <v-icon color="green" small>mdi-arrow-up</v-icon>
            <span class="text-success font-weight-bold ml-1">2.36%</span>
            <div class="text-h5 font-weight-bold text-white">30,00,000 ₩</div>
        </v-col>
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
    name: "TotalSaving",
  };
  </script>

<style scoped>

.portfolio-card {
    min-width: 330px;
    text-align: center;
}

.container-custom {
    background-color: #517FF5;
}
</style>