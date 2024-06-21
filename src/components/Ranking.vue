<template>
  <v-card class="ma-2">
    <div class="d-flex flex-no-wrap justify-space-between align-center ma-5">
      <div class="mx-10">
        <v-table density="compact">
          <thead>
            <tr>
              <th class="text-left">姓名</th>
              <th class="text-left">分數</th>
              <th class="text-left">名次</th>
            </tr>
        </thead>
          <tbody>
            <tr v-for="ranking in rankings" :key="ranking.name">
              <td>{{ ranking.name }}</td>
              <td>{{ ranking.score }}</td>
              <td>{{ ranking.rank }}</td>
            </tr>
          </tbody>
        </v-table>
      </div>
    </div>
  </v-card>
</template>


<script>
  export default {
    data () {
      return {
        rankings: [
          {
            name: '何語婕',
            score: 96,
            rank: 1,
          },
          {
            name: '游騰恩',
            score: 86,
            rank: 2,
          },
          {
            name: '孫鴻民',
            score: 74,
            rank: 3,
          },
          {
            name: '何璟威',
            score: 66,
            rank: 4,
          },
          {
            name: '謝和軒',
            score: 58,
            rank: 5,
          },
          {
            name: '謝和羲',
            score: 56,
            rank: 5,
          },
          {
            name: '張瑄旂',
            score: 50,
            rank: 7,
          },
        ],
      }
    },
  }
</script>
