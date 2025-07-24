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
    year: '2015',
    title: '東京大学 入学',
    description: '情報工学部でプログラミングを学ぶ'
  },
  {
    year: '2019',
    title: '株式会社A 入社',
    description: 'フロントエンドエンジニアとしてVue.js開発に従事'
  },
  {
    year: '2022',
    title: '株式会社B 転職',
    description: 'フルスタックエンジニアとしてバックエンドにも挑戦'
  }
]
</script>
