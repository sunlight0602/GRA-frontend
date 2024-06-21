<template>
  <v-card class="ma-2">
    <div class="d-flex flex-no-wrap justify-space-between align-center ma-5">
      <div>
        <v-card-subtitle>測驗日期：2023/07/13</v-card-subtitle>
        <v-card-title class="text-h5">第１次全民中檢仿真模擬考</v-card-title>
        <v-card-actions>
          <v-btn class="ms-2" size="small" variant="outlined">
            刪除此考卷
          </v-btn>
          <v-btn class="ms-2" size="small" variant="outlined">
            下載所有成績單
          </v-btn>
          <v-btn class="ms-2" size="small" variant="outlined">
            瀏覽老師成績單
          </v-btn>
        </v-card-actions>
      </div>
      
      <div class="mx-10">
        <v-table density="compact">
          <tbody>
            <tr v-for="percentage in percentages" :key="percentage.item">
              <td>{{ percentage.item }}</td>
              <td>{{ percentage.score }}</td>
            </tr>
          </tbody>
        </v-table>
      </div>

      <div class="mx-6">
        <v-table density="compact">
          <tbody>
            <tr v-for="error in errors" :key="error.item">
              <td>{{ error.item }}</td>
              <td>{{ error.quant }} 題</td>
              <td>{{ error.correct }} 題／人</td>
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
        percentages: [
          {
            item: '頂標',
            score: 96,
          },
          {
            item: '前標',
            score: 86,
          },
          {
            item: '均標',
            score: 66,
          },
          {
            item: '後標',
            score: 58,
          },
        ],
        errors: [
          {
            item: '形音義',
            quant: 8,
            correct: 4.43,
          },
          {
            item: '詞語使用',
            quant: 8,
            correct: 5.29,
          },
          {
            item: '成語運用',
            quant: 8,
            correct: 6.86,
          },
          {
            item: '修辭技巧',
            quant: 8,
            correct: 5.29,
          },
          {
            item: '國學常識',
            quant: 8,
            correct: 5.71,
          },
          {
            item: '閱讀素養',
            quant: 10,
            correct: 7.14,
          },
        ],
      }
    },
  }
</script>
