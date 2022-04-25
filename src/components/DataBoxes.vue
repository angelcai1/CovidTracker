<template>
    <div class="grid md:grid-cols-2 gap-4">
        <!-- Cases Box -->
        <div class="shadow-md bg-red-100 border-4 border-red-200 p-10 text-center rounded">
            <h3 class="text-3xl text-blue-900-font-bold mb-4">
                Cases
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">
                    New:
                </span>
                {{ numbersWithCommas(stats.NewConfirmed) }}
            </div>
            <div class="text-2xl mb-4">
                
                <span class="font-bold">
                    Total:
                </span>
                {{ numbersWithCommas(stats.TotalConfirmed) }}
            </div>
            
        </div>
        <!-- Deaths Box -->
        <div class="shadow-md bg-red-200 border-4 border-red-300 p-10 text-center rounded">
            <h3 class="text-3xl text-blue-900-font-bold mb-4">
                Deaths
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">
                    New:
                </span>
                {{ numbersWithCommas(stats.NewDeaths) }}
            </div>
            <div class="text-2xl mb-4">
                
                <span class="font-bold">
                    Total:
                </span>
                {{ numbersWithCommas(stats.TotalDeaths) }}
            </div>
            
        </div>
    </div>
</template>
<script>
    export default {
        name: 'DataBoxes',
        props: ['stats'],
        methods: {
            numbersWithCommas(x) {
                return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
            }
        }
    }
</script>