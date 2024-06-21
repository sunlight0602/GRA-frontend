<script setup>
import Title from './components/Title.vue'
import Index from './components/Index.vue';
import ExamInfo from './components/ExamInfo.vue';
import Ranking from './components/Ranking.vue';
</script>

<template>
  <v-layout class="rounded rounded-md">
    <v-app-bar title="考卷批改＆成績單生成">
      <Title />
    </v-app-bar>
  
    <v-navigation-drawer>
      <Index />
    </v-navigation-drawer>

    <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
      <v-container>
        <v-row align="center" justify="center">
          <ExamInfo />
        </v-row>
        <v-row align="center" justify="center">
          <Ranking />
        </v-row>
      </v-container>

    </v-main>
  </v-layout>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>./components/ExamInfo.vue./components/Ranking.vue
