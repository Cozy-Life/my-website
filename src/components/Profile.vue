<template>
  <section class="bg-white shadow-xl rounded-xl p-4 sm:p-8 max-w-3xl mx-auto">
    <div class="flex flex-col items-center">
      <img
        src="/src/assets/me_image.jpg"
        alt="プロフィール画像"
        class="w-48 sm:w-90 h-48 sm:h-70 rounded-full border-4 border-indigo-500 shadow-md mb-2 sm:mb-4"
      />
      <h2 class="text-2xl font-bold text-indigo-600 mb-1 sm:mb-2">岡田 孟</h2>
      <p class="text-gray-700 text-center mb-2 sm:mb-4">
        ソフトウェアエンジニア
      </p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 gap-2 sm:gap-4 mt-2 sm:mt-6 text-gray-800">
      <div class="bg-indigo-50 rounded-lg p-2 sm:p-4">
        <h3 class="text-sm font-semibold text-indigo-500">出身地</h3>
        <p>神奈川県</p>
      </div>
      <div class="bg-indigo-50 rounded-lg p-2 sm:p-4">
        <h3 class="text-sm font-semibold text-indigo-500">生年月日</h3>
        <p>1997年6月20日</p>
      </div>
      <div class="bg-indigo-50 rounded-lg p-2 sm:p-4">
        <h3 class="text-sm font-semibold text-indigo-500">趣味</h3>
        <p>お笑い、サッカー観戦、アニメ鑑賞</p>
      </div>
      <div class="bg-indigo-50 rounded-lg p-2 sm:p-4">
        <h3 class="text-sm font-semibold text-indigo-500">好きな言語</h3>
        <p>JavaScript / Java / TypeScript</p>
      </div>
    </div>
  </section>
</template>
