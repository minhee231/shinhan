<template>
    <v-card class="pa-4" outlined>
      <v-card-title>
        Statistics
        <v-spacer></v-spacer>
        <v-select
          v-model="selectedPeriod"
          :items="timePeriods"
          label="Select Period"
          outlined
          dense
          class="ma-2"
        ></v-select>
      </v-card-title>
      <v-card-subtitle class="text-caption grey--text">
        <v-icon dense>mdi-circle</v-icon> Investment
        <v-icon dense class="ml-2" color="green">mdi-circle</v-icon> Earnings
      </v-card-subtitle>
      <v-card-text>
        <Bar :chart-data="chartData" :options="chartOptions" />
      </v-card-text>
    </v-card>
  </template>
  
  <script>
  import { Bar } from 'vue-chartjs';
  import { Chart as ChartJS, CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend } from 'chart.js';
  
  // Register necessary components for ChartJS
  ChartJS.register(CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend);
  
  export default {
    components: {
      Bar
    },
    data() {
      return {
        selectedPeriod: 'Last 7 days',
        timePeriods: ['Last 7 days', 'Last 30 days', 'This year'],
        chartData: {
          labels: ['1/1', '1/2', '1/3', '1/4', '1/5', '1/6', '1/7'],
          datasets: [
            {
              label: 'Investment',
              backgroundColor: '#4CAF50',
              data: [2000, 1500, 1000, 2500, 500, 1800, 1200]
            },
            {
              label: 'Earnings',
              backgroundColor: '#E0E0E0',
              data: [1000, 2000, 500, 2000, 1500, 1000, 3000]
            }
          ]
        },
        chartOptions: {
          responsive: true,
          maintainAspectRatio: false,
          scales: {
            y: {
              beginAtZero: true,
              max: 3000
            }
          },
          plugins: {
            legend: {
              display: true,
              position: 'top'
            }
          }
        }
      };
    }
  };
  </script>
  
  <style scoped>
  .v-select .v-input__control {
    min-width: 150px;
  }
  </style>
  