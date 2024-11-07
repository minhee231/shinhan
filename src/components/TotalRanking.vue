<template>
    <v-expansion-panels class="pa-4 rounded-panels bg-white" variant="popout">
        <v-container class="fill-height" fluid>
            <v-row class="justify-center align-center">
                <v-card class="container-custom portfolio-card rounded-xl" outlined>
                    <v-col class="text-center d-flex justify-center align-center mb-2">
                        <div class="text-h6 font-weight-bold text-white">순위</div>
                        <v-divider :thickness="180" vertical></v-divider>
                        <v-icon color="white" small>mdi-arrow-up-drop-circle</v-icon>
                        <v-divider :thickness="10" vertical></v-divider>
                        <v-icon color="white" small>mdi-arrow-down-drop-circle</v-icon>
                    </v-col>
                    <v-col class="pa-0">
                        <v-card class="ranking-card rounded-xl" outlined>
                            <v-simple-table class="ranking-table">
                                <thead>
                                    <tr>
                                        <th class="text-center">순위</th>
                                        <th class="text-center">이름</th>
                                        <th class="text-center">수익</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td class="text-center">1</td>
                                        <td class="text-center">성유영</td>
                                        <td class="text-center">23%</td>
                                    </tr>
                                    <tr>
                                        <td class="text-center">2</td>
                                        <td class="text-center">구민희</td>
                                        <td class="text-center">0%</td>
                                    </tr>
                                    <tr>
                                        <td class="text-center">3</td>
                                        <td class="text-center">현성</td>
                                        <td class="text-center">-8%</td>
                                    </tr>
                                </tbody>
                            </v-simple-table>
                        </v-card>
                    </v-col>
                </v-card>
            </v-row>
        </v-container>
    </v-expansion-panels>
</template>

<script>
export default {
    name: "TotalRanking",
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

.ranking-card {
    background-color: #ffffff;
}

.ranking-table {
    width: 1483%; /* 테이블 전체 너비 설정 */
    height: 100%;
    border-collapse: collapse;
    
}

.ranking-table th, .ranking-table td {
    padding: 8px;
    width: 350px;
    border: 1px solid #517FF5;
}

.ranking-table th {
    background-color: #3B6BFF;
    color: #fff;
}

.ranking-table tbody tr:nth-child(odd) {
    background-color: #e1e1e1;
}

.ranking-table tbody tr:nth-child(even) {
    background-color: #ffffff;
}

.ranking-table td {
    text-align: center;
    font-weight: bold;
}
</style>
