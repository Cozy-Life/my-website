<template>
  <section class="bg-white shadow-xl rounded-xl p-8 max-w-3xl mx-auto">
    <div class="flex flex-col items-center">
      <img
        src="/src/assets/vue.svg"
        alt="プロフィール画像"
        class="w-32 h-32 rounded-full border-4 border-indigo-500 shadow-md mb-4"
      />
      <h2 class="text-2xl font-bold text-indigo-600 mb-2">岡田 武</h2>
      <p class="text-gray-700 text-center mb-4">
        フロントエンドエンジニア / Vue.js & Tailwind CSS 好き。ユーザーにやさしいUIをつくるのが得意です。
      </p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mt-6 text-gray-800">
      <div class="bg-indigo-50 rounded-lg p-4">
        <h3 class="text-sm font-semibold text-indigo-500">出身地</h3>
        <p>東京都</p>
      </div>
      <div class="bg-indigo-50 rounded-lg p-4">
        <h3 class="text-sm font-semibold text-indigo-500">生年月日</h3>
        <p>1994年5月20日</p>
      </div>
      <div class="bg-indigo-50 rounded-lg p-4">
        <h3 class="text-sm font-semibold text-indigo-500">趣味</h3>
        <p>カフェ巡り、写真、アニメ鑑賞</p>
      </div>
      <div class="bg-indigo-50 rounded-lg p-4">
        <h3 class="text-sm font-semibold text-indigo-500">好きな言語</h3>
        <p>JavaScript / TypeScript</p>
      </div>
    </div>
  </section>
</template>
