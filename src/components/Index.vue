<template>
  <v-card class="mx-auto" max-width="300">
    <v-list :items="exams"></v-list>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      exams: [
        { type: 'subheader', title: '考卷清單' },
        {
          title: '第１次全民中檢仿真模擬考',
          value: 1,
        },
        {
          title: '第 2 次全民中檢仿真模擬考',
          value: 2,
        },
        {
          title: '第 3 次全民中檢仿真模擬考',
          value: 3,
        },
        {
          title: '第 4 次全民中檢仿真模擬考',
          value: 4,
        },
        {
          title: '第五次全民中檢仿真模擬考',
          value: 5,
        },
        { type: 'divider' },
        { type: 'subheader', title: '使用說明' },
      ],
    }),
  }
</script>