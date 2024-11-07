<template>
  <v-app>
    <v-main>
      <!-- 성 유 영 님! 저한테 정말 그러시면 안되는거죠~<br>
      아니 어떻게 제출 하루전에 프론트를 짜라고 하실 수 있어요~!~! -->
      <div class="">
        <UserProfile/>
        <TotalPortfolio/>
        <TotalSaveing/>
        <TotalRanking/>
      </div>
      <FooterMenu />
    </v-main>
  </v-app>
</template>

<script>
import FooterMenu from './components/FooterMenu.vue';
import UserProfile from './components/UserProfile.vue';
import TotalPortfolio from './components/TotalPortfolio.vue';
import TotalSaveing from './components/TotalSaveing.vue';
import TotalRanking from './components/TotalRanking.vue';

export default {
  name: 'App',

  components: {
    FooterMenu,
    UserProfile,
    TotalPortfolio,
    TotalSaveing,
    TotalRanking,
  },

  data: () => ({}),
}
</script>

<style scoped>
  /* 컨텐츠 영역 */
  .content {
    max-height: 800px; /* 페이지가 화면을 다 채우도록 설정 */
    padding-bottom: 56px; /* 푸터와 겹치지 않도록 여백 추가 */
    overflow-y: auto; /* 내용이 많을 경우 스크롤을 생성 */
  }


  
</style>
