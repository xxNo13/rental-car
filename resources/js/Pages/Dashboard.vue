<script setup>
import Navbar from '@/Layouts/Navbar.vue';
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    cars: {
        type: Array,
    }
});

</script>

<template>
    <Head title="Dashboard" />

    <Navbar>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">Dashboard</h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-sm sm:rounded-lg py-10 px-5">
                    <div class="grid grid-cols-3 gap-4">
                        <div class="max-w-sm rounded overflow-hidden shadow-lg" v-for="car in cars" :key="car.id">
                            <div class="bg-gray-300">
                                <img class="w-full" src="" style="height: 150px;" alt="Sunset in the mountains">
                            </div>
                            <div class="px-6 py-4">
                                <div class="font-bold text-xl mb-2">
                                    {{ car.car_name }} - {{ car.car_brand }}
                                </div>
                                <p class="text-gray-700 text-base">
                                    {{ car.plate_number }}
                                </p>
                            </div>
                            <div class="px-6 pt-4 pb-2">
                                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#photography</span>
                                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#travel</span>
                                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#winter</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>  
        </div>
    </Navbar>
</template>
