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
        
        <div>
            <p>{{product.title}}</p>
            <p>{{product.price}}</p>
            <p>{{product.id}}</p>
        </div>
    </div>
</template>

<script setup>
    const { id } = useRoute().params
    const uri = 'https://fakestoreapi.com/products/' + id

    const { data: product } = await useFetch(uri, {key:id})
</script>

<style scoped>

</style>