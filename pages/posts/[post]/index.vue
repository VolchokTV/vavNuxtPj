<template>
    <div>
        POST{{route.params.post}}

    </div>
</template>

<script setup lang="ts">
    definePageMeta({ layout: "post" });
    const route = useRoute();

</script>

<style scoped>

</style>