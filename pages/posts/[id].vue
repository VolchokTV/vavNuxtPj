<template>
    <div>
        <div v-if="status === 'pending'">Loading...</div>
        <div v-else> 
            <p> POST ID: {{id}} </p>
            <p> POST title: {{post.title}} </p>
            <p> POST body: {{post.body}} </p>
        </div>
     </div>
</template>

<script setup lang="ts">
    definePageMeta({ layout: "post" });
    const {id} = useRoute().params;

    interface IPost{
        id: number,
        body: string,
        title: string
    }
    // получаем данные поста по его айдишнику
    const {data: post, status} = await useFetch<IPost>("https://jsonplaceholder.typicode.com/posts/" + id);
</script> 

<style scoped>

p {
    font-size: 18px;
}

</style>