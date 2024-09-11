<template>
    <ShopNavbar />
    <ProductLayout :products="productsApi" />
</template>

<script lang="ts" setup>
//components
import ProductLayout from '../components/products/ProductLayout.vue';
import ShopNavbar from '../components/ShopNavbar.vue';
//from vue
import { ref } from 'vue';
import type { Product } from '../interfaces/Product.interface';

const productsApi = ref<Product[]>([]);

const getDataFromApi = async () => {
    const url = "https://dummyjson.com/products";
    const response = await fetch(url);
    const data = await response.json();
    const { products } = data
    productsApi.value = products;
}
getDataFromApi();


</script>