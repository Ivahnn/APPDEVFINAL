<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import Carousel from '@/Components/Carousel.vue';
import { Head, Link, router } from '@inertiajs/vue3';
import { watch, ref, onMounted, defineProps } from 'vue';
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    BarElement,
    CategoryScale,
    LinearScale,
    ArcElement,
} from 'chart.js'
import { Bar, Pie } from 'vue-chartjs'

ChartJS.register(CategoryScale, ArcElement, LinearScale, BarElement, Title, Tooltip, Legend)

const props = defineProps({
    busTypes: Object,
    busCapacity: Object,
    busRoutes: Object,
});

console.log('Fetched Bus Types:', props.busRoutes);

const chartData = ref({
  labels: Object.keys(props.busRoutes),
  datasets: [
    {
      label: 'Bus Routes',
      data: Object.values(props.busRoutes),
      backgroundColor: Object.values(props.busRoutes).map(() => getRandomColor()),
    },
  ],
});

// Function to generate a random color
function getRandomColor() {
  const letters = '0123456789ABCDEF';
  let color = '#';
  for (let i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}

const chartData1 = ref({
    labels: Object.keys(props.busCapacity),
    datasets: [
        {
        label: 'Bus Capacity',
        data:  Object.values(props.busCapacity),
        backgroundColor: Object.values(props.busRoutes).map(() => getRandomColor()),
        },
    ],
});
const busRouteLabels = Object.keys(props.busTypes);
const busRoutesData = Object.values(props.busTypes);

const data = {
    labels: busRouteLabels,
    datasets: [
        {
            label: 'Bus Type',
            data: busRoutesData,
            backgroundColor: Object.values(props.busRoutes).map(() => getRandomColor()),
        }
    ]
}

const chartOptions = ref({
    responsive: true,
});
const options = ref({
    maintainAspectRatio: false
});
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <div class="flex justify-center">
            <div class="p-6 dark:border-gray-700 mt-14">
                <div class="grid grid-cols-2 md:grid-cols-2 gap-4">
                    
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 bg-sky-200 p-6 rounded-xl">
                        <Bar :data="chartData" :options="chartOptions" />
                    </div>
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 bg-sky-200 p-6 rounded-xl">
                        <Bar :data="chartData1" :options="chartOptions" />
                    </div>
                </div>
                <div class="flex flex-col items-center">
                    <div class="bg-sky-200 p-6 w-[500px] rounded-xl my-5">
                        <div class="items-center">
                            <legend>Bus Routes</legend>
                            <div class="w-full md:w-auto">
                                <Pie :data="data" :options="options" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </AuthenticatedLayout>
  >

</template>