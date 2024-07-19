<template>
    <div>
        <DataTable paginator :rows="5"  :value="products" >
            <Column field="id" header="Id"></Column>
            <Column field="name" header="Name"></Column>
            <Column field="category" header="Category"></Column>
            <Column field="rating" header="Rating"></Column>
        </DataTable>
    </div>
</template>
<script setup>
import { ref, onMounted } from 'vue';
import { ProductService } from '@/service/ProductService';

onMounted(() => {
    ProductService.getProducts().then((data) => (products.value = data));
});

const products = ref();
</script>