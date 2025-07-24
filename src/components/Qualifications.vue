<template>
  <section class="bg-white shadow-xl shadow-indigo-200/40 rounded-xl p-8 max-w-3xl mx-auto">
    <h2 class="text-2xl font-semibold mb-6 text-indigo-600">資格</h2>
    <ul class="space-y-6">
      <li
        v-for="qual in qualifications"
        :key="qual.name"
        class="border-l-4 border-indigo-500 pl-5"
      >
        <h3 class="text-xl font-bold text-indigo-700">{{ qual.name }}</h3>
        <p class="text-sm text-gray-600 mb-1">{{ qual.date }}</p>
      </li>
    </ul>
  </section>
</template>

<script setup>
const qualifications = [
  {
    name: 'ITパスポート',
    date: '2021年2月',
  },
  {
    name: '基本情報技術者試験',
    date: '2021年10月',
  },
  {
    name: 'Java Silver SE11',
    date: '2021年12月',
  },
  {
    name: 'Java Gold SE11',
    date: '2022年2月',
  },
  {
    name: '応用情報技術者試験',
    date: '2022年4月',
  },
  {
    name: 'FP3級',
    date: '2025年7月',
  }
]
</script>
