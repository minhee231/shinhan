<template>
  <v-expansion-panels class="pa-4 rounded-panels bg-white"  variant="popout">
  <v-container class="fill-height" fluid>
    <v-row class="justify-center align-center">
      <v-col cols="auto">
        <v-card class="portfolio-card pa-4 d-flex flex-column align-center rounded-xl container-custom">
          <v-row class="d-flex justify-center align-center mb-2">
            <span class="text-subtitle-2 font-weight-bold text-white">포트폴리오(총 자산)</span>
            <v-spacer></v-spacer>
            <v-icon color="green" small class="bordered-icon">mdi-arrow-up</v-icon>
            <span class="text-success font-weight-bold ml-1">2.36%</span>
          </v-row>

          <!-- Main Amount -->
          <v-row class="justify-center">
            <span class="text-h4 font-weight-bold text-white">57,401,490 ₩</span>
          </v-row>

          <v-divider class="my-4"></v-divider>

          <v-row class="d-flex justify-center align-center">
            <v-col class="text-center">
              <v-icon color="green" small>mdi-arrow-up</v-icon>
              <span class="text-body-2 font-weight-bold text-white">수익</span>
              <div class="text-h6 font-weight-bold text-white">30,401,490 ₩</div>
            </v-col>

            <v-divider vertical></v-divider>
            <v-divider vertical></v-divider>
            <v-divider vertical></v-divider>

            <v-col class="text-center">
              <v-icon color="red" small>mdi-arrow-down</v-icon>
              <span class="text-body-2 font-weight-bold text-white">투자</span>
              <div class="text-h6 font-weight-bold text-white">27,000,000 ₩</div>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
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
  min-width: 330px;
  text-align: center;
}

.container-custom {
  background-color: #517FF5;
}

.bordered-icon {
  border-radius: 50%;
}
</style>
