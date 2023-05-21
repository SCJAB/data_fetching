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

        <h2 class="font-bold text-2xl">WELCOME TO FAKESTOREAPI</h2>
    </div>
</template>

<script setup>

</script>

<style scoped>
    h2
    {
        margin-top: 15%;
        text-align: center;
    }
    .router-link-exact-active
    {
        color: crimson;
    }
</style>