<template>
    <!-- component -->
    <div class="py-6 mr-6">
        <div class="flex max-w-md bg-white shadow-lg rounded-lg overflow-hidden">
            <img class="w-1/3 bg-cover" :src='images[0]' />
            <div class="w-2/3 p-4">
                <h1 class="text-gray-900 font-bold text-2xl">{{ title }}</h1>
                <blockquote class="text-slate-500">{{ category }}</blockquote>
                <p class="mt-2 text-gray-600 text-sm">{{ description }}</p>

                <div class="flex item-center justify-between mt-3">
                    <h1 class="text-gray-700 font-bold text-xl">{{ price }}</h1>
                    <button class="px-3 py-2 bg-gray-800 text-white text-xs font-bold uppercase rounded">Add to
                        Card</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { defineProps } from 'vue';
interface Props {
    title: string
    description: string
    category: string
    price: number
    images: string[]
}

defineProps<Props>();
</script>
