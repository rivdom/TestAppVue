<template>
    <div class="flex p-8 flex-wrap justify-evenly">
        <ProductCard v-for="product in products" :key="product.id" v-bind="product" />


    </div>


</template>

<script lang="ts" setup>
import ProductCard from './ProductCard.vue';
import { defineProps } from 'vue';
import type { Product } from '../../interfaces/Product.interface';

interface Props {
    products: Product[];
}

const { products } = defineProps<Props>();
</script>