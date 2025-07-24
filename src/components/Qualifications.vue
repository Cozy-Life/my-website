<template>
  <section class="bg-white shadow-xl shadow-indigo-200/40 rounded-xl p-8 max-w-3xl mx-auto">
    <h2 class="text-2xl font-semibold mb-6 text-indigo-600">資格・受賞歴</h2>
    <ul class="space-y-6">
      <li
        v-for="qual in qualifications"
        :key="qual.name"
        class="border-l-4 border-indigo-500 pl-5"
      >
        <h3 class="text-xl font-bold text-indigo-700">{{ qual.name }}</h3>
        <p class="text-sm text-gray-600 mb-1">{{ qual.date }}</p>
        <p class="text-gray-700">{{ qual.description }}</p>
      </li>
    </ul>
  </section>
</template>

<script setup>
const qualifications = [
  {
    name: '基本情報技術者試験',
    date: '2020年6月',
    description: 'ITの基礎知識を問う国家資格。プログラミングやネットワークの基礎が身についています。'
  },
  {
    name: '応用情報技術者試験',
    date: '2022年11月',
    description: 'より高度なIT技術やプロジェクト管理の知識を問う国家資格。実務経験を積む上で役立ちます。'
  },
  {
    name: 'TOEIC 900点',
    date: '2021年9月',
    description: 'ビジネス英語の能力を示すスコア。海外とのコミュニケーションにも対応可能です。'
  }
]
</script>
