<template>
    <section class="bg-white shadow-xl shadow-indigo-200/40 rounded-xl p-8 max-w-3xl mx-auto">
        <h2 class="text-2xl font-semibold mb-6 text-indigo-600">スキル習得推移 </h2>
        <div class="p-8　relative h-[500px]">
            <Line :data="chartData" :options="chartOptions" />
        </div>
    </section>
</template>

<script setup>
import { Line } from 'vue-chartjs'
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  LineElement,
  PointElement,
  CategoryScale,
  LinearScale
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, LineElement, PointElement, CategoryScale, LinearScale)

const chartData = {
  labels: ['2021', '2022', '2023', '2024', '2025'],
  datasets: [
    {
      label: 'JavaScript',
      borderColor: '#facc15',
      backgroundColor: '#fde68a',
      data: [0, 0, 30, 45, 55],
      tension: 0.3
    },
    {
      label: 'Java',
      borderColor: '#3b82f6',
      backgroundColor: '#93c5fd',
      data: [20, 40, 50, 55, 60],
      tension: 0.3
    },
    {
      label: 'Vue.js',
      borderColor: '#10b981',
      backgroundColor: '#6ee7b7',
      data: [0, 0, 0, 40, 45, 55],
      tension: 0.3
    },
    {
      label: 'SpringBoot',
      borderColor: '#ef4444',
      backgroundColor: '#fca5a5',
      data: [0, 0, 40, 45, 50, 55],
      tension: 0.3
    }
  ]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  plugins: {
    legend: { position: 'top' },
    title: { display: false }
  },
  scales: {
    y: {
      suggestedMin: 0,
      suggestedMax: 100,
      title: {
        display: true,
        text: '経験 (%)'
      }
    },
    x: {
      title: {
        display: true,
        text: '年度'
      }
    }
  }
}
</script>

<style scoped>
    canvas {
    height: 100% !important;
    width: 100% !important;
    }
</style>
