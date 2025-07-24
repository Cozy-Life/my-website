<template>
  <main class="min-h-screen bg-gray-100 p-8">
    <div class="max-w-3xl mx-auto">

      <!-- タブボタン -->
      <div class="flex space-x-4 border-b border-gray-300 mb-8">
      <button
          @click="activeTab = 'home'"
          :class="activeTab === 'home'
            ? 'border-b-4 border-blue-600 text-blue-700 font-semibold'
            : 'text-gray-600 hover:text-blue-600'"
          class="pb-3 px-6 transition-colors duration-300"
        >
          ホーム
        </button>
        <button
          @click="activeTab = 'timeline'"
          :class="activeTab === 'timeline'
            ? 'border-b-4 border-blue-600 text-blue-700 font-semibold'
            : 'text-gray-600 hover:text-blue-600'"
          class="pb-3 px-6 transition-colors duration-300"
        >
          経歴
        </button>
        <button
          @click="activeTab = 'skill'"
          :class="activeTab === 'skill'
            ? 'border-b-4 border-blue-600 text-blue-700 font-semibold'
            : 'text-gray-600 hover:text-blue-600'"
          class="pb-3 px-6 transition-colors duration-300"
        >
          スキル
        </button>
        <button
          @click="activeTab = 'qualifications'"
          :class="activeTab === 'qualifications'
            ? 'border-b-4 border-blue-600 text-blue-700 font-semibold'
            : 'text-gray-600 hover:text-blue-600'"
          class="pb-3 px-6 transition-colors duration-300"
        >
          資格
        </button>
        <button
          @click="activeTab = 'contact'"
          :class="activeTab === 'contact'
            ? 'border-b-4 border-blue-600 text-blue-700 font-semibold'
            : 'text-gray-600 hover:text-blue-600'"
          class="pb-3 px-6 transition-colors duration-300"
        >
          連絡先
        </button>
      </div>

      <!-- タブ内容カード -->
      <section
        v-if="activeTab === 'home'"
        class="bg-white shadow-lg rounded-xl p-8 transition-opacity duration-500"
      >
        <Profile />
      </section>

      <section
        v-if="activeTab === 'timeline'"
        class="bg-white shadow-lg rounded-xl p-8 transition-opacity duration-500"
      >
        <Timeline />
      </section>

      <section
        v-if="activeTab === 'skill'"
        class="bg-white shadow-lg rounded-xl p-8 transition-opacity duration-500"
      >
        <SkillProgressChart />
      </section>

      <section
        v-if="activeTab === 'qualifications'"
        class="bg-white shadow-lg rounded-xl p-8 transition-opacity duration-500"
      >
        <Qualifications />
      </section>

      <section
        v-if="activeTab === 'contact'"
        class="bg-white shadow-lg rounded-xl p-8 transition-opacity duration-500"
      >
        <ContactInfo />
      </section>
    </div>
  </main>
</template>

<script setup>
import { ref } from 'vue'
import Profile from './components/Profile.vue'
import Timeline from './components/Timeline.vue'
import SkillProgressChart from './components/SkillProgressChart.vue'
import Qualifications from './components/Qualifications.vue'
import ContactInfo from './components/ContactInfo.vue'

const activeTab = ref('timeline')
</script>
