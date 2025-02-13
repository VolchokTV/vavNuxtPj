<template>
    <H3>  Posts : </H3>
    <ul>
        <li v-if="status === 'pending'">Loading...</li>
   
        <li v-else class="posts" v-for="post in posts" :key="post.id">
            {{ post.title }}
        </li>
    </ul>

</template>

<script setup lang="ts">
    definePageMeta({ layout: "posts" });
    interface IPost{
        id: number,
        title: string
    }

const {
  data: posts,
  error,
  status,
} = useLazyFetch<IPost[]>("https://jsonplaceholder.typicode.com/posts");


</script>

<style scoped>
div {
  font-size: 40px;
  font-weight: 700;
  color: green;
}
.posts {
  padding-left: 20px;
    color: black;
  font-weight: 500;
  font-size: 24px;
}
</style>