<template>
    <div>
        MainPage
        <nav>
            <ul>
                <li><NuxtLink to="/about">About</NuxtLink></li>
                <li><NuxtLink to="/posts">Posts</NuxtLink></li>
            </ul>
        </nav>
    </div>
</template>

<script setup lang="ts">
definePageMeta({ layout: "default" });
</script>

<style scoped>

</style>