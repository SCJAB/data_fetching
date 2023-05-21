<template>
    <div class="font-sans">
        <header class="font-semibold">
            <nav class="m-3">
                <ul class="flex gap-4">
                    <li><nuxt-link to="/">Home</nuxt-link></li>
                    <li><nuxt-link to="/products">Products</nuxt-link></li>
                </ul>
            </nav>
        </header>
        
        <div class="grid grid-cols-3 gap-10 m-16">
            <div v-for="p in products">
                <nuxt-link :to="`/products/${p.id}`">{{p.title}}</nuxt-link>
            </div>
        </div>
    </div>
</template>

<script setup>
    const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>
    .router-link-exact-active
    {
        color: crimson;
    }
</style>