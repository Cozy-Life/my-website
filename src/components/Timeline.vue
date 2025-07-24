<template>
  <div class="relative border-l-4 border-blue-600 pl-8 ml-4 space-y-10 max-w-xl mx-auto">
    <motion
      v-for="(item, index) in timeline"
      :key="item.year"
      class="relative block"
      v-motion
      :initial="{ opacity: 0, x: -50 }"
      :enter="{ opacity: 1, x: 0 }"
      :transition="{ delay: index * 0.6, duration: 1.2, easing: 'ease-out' }"
    >
      <div
        class="absolute -left-7 top-1 w-5 h-5 bg-blue-600 rounded-full shadow-lg"
      ></div>
      <div class="mb-1 text-sm text-gray-400 font-mono tracking-wide">{{ item.year }}</div>
      <div class="text-xl font-semibold text-blue-700">{{ item.title }}</div>
      <p class="text-gray-700 mt-1">{{ item.description }}</p>
    </motion>
  </div>
</template>

<script setup>
const timeline = [
  {
    year: '2016',
    title: '横浜国立大学 入学',
    description: 'プログラミングを学ぶ'
  },
  {
    year: '2021',
    title: '受託システム開発会社に入社',
    description: '自動倉庫のシステム開発に携わる'
  },
  {
    year: '2023',
    title: '独立 1社目',
    description: '証券会社のWebアプリ開発に携わる'
  },
  {
    year: '2024',
    title: '独立 2社目',
    description: 'モバイル会社のWebアプリ開発に携わる'
  },
  {
    year: '2025',
    title: '独立 2社目',
    description: '上記のシステム開発を継続'
  }
]
</script>
