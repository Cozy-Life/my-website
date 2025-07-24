<template>
  <div class="bg-white rounded-xl shadow p-4">
    <h2 class="text-xl font-bold mb-4">スキル習得推移</h2>
    <Line :data="chartData" :options="chartOptions" />
  </div>
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
  labels: ['2019', '2020', '2021', '2022', '2023', '2024'],
  datasets: [
    {
      label: 'JavaScript',
      borderColor: '#facc15',
      backgroundColor: '#fde68a',
      data: [20, 40, 60, 75, 85, 95],
      tension: 0.3
    },
    {
      label: 'Vue.js',
      borderColor: '#3b82f6',
      backgroundColor: '#93c5fd',
      data: [0, 20, 40, 65, 80, 90],
      tension: 0.3
    },
    {
      label: 'Tailwind CSS',
      borderColor: '#10b981',
      backgroundColor: '#6ee7b7',
      data: [0, 10, 30, 60, 80, 95],
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
        text: 'スキルレベル (%)'
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
div {
  height: 400px;
}
</style>
