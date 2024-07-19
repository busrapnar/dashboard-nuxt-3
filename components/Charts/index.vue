<template>
    <Chart type="bar" :data="chartData" :options="chartOptions" class="max-w-4xl h-[30rem]"  />
</template>
<script setup>
import Chart from 'primevue/chart';
onMounted(() => {
    chartData.value = setChartData();
    chartOptions.value = setChartOptions();
});

const chartData = ref();
const chartOptions = ref();

const setChartData = () =>  {
    const documentStyle = getComputedStyle(document.documentElement);

    return {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
        datasets: [
            {
                type: 'bar',
                label: 'Personal Wallet',
                backgroundColor: ('#989898'),
                borderRadius: '4px',
                data: [50, 25, 12, 48, 90, 76, 42, 25, 12, 48, 90, 98]
            },
            {
                type: 'bar',
                label: 'Corporate Wallet',
                backgroundColor: ('#d3d3d3'),
                data: [21, 84, 24, 75, 37, 65, 34, 75, 37, 65, 34, 65]
            },
            {
                type: 'bar',
                label: 'Investment Wallet',
                backgroundColor: ('#e9e9e9'),
                data: [41, 52, 24, 74, 23, 21, 32, 41, 52, 24, 74, 23]
            }
        ]
    };
};
const setChartOptions = () =>  {
    const documentStyle = getComputedStyle(document.documentElement);
    const textColor = documentStyle.getPropertyValue('--p-text-color');
    const textColorSecondary = documentStyle.getPropertyValue('--p-text-muted-color');
    const surfaceBorder = documentStyle.getPropertyValue('--p-content-border-color');

    return {
        maintainAspectRatio: false,
        aspectRatio: 0.8,
        plugins: {
            tooltips: {
                mode: 'index',
                intersect: false
            },
            legend: {
                labels: {
                    color: textColor
                }
            }
        },
        scales: {
            x: {
                stacked: true,
                ticks: {
                    color: textColorSecondary
                },
                grid: {
                    color: surfaceBorder
                }
            },
            y: {
                stacked: true,
                ticks: {
                    color: textColorSecondary
                },
                grid: {
                    color: surfaceBorder
                }
            }
        }
    };
}
</script>