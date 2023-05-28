<template>
    <div class="card text-center">
        <img :src="product.image" alt="product thumb" class="thumb">
        <p class="text-center">{{product.title}} <br> {{ product.price }}</p>
        <nuxt-link :to="`/products/${product.id}`"></nuxt-link>
    </div>
</template>

<script setup>
    const { product } = defineProps(['product'])
</script>

<style scoped>
.thumb
{
    max-height: 120px;
    max-width: 70%;
    margin: 0 auto;
}
</style>