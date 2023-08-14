<script setup>
const route = useRoute();
const { data: post } = await useFetch(
  `https://jsonplaceholder.typicode.com/posts/${route.params.id}`
);
</script>

<template>
  <div>
    <h3 class="text-bold">Title:{{ post.title }}</h3>
    <p>{{ post.body }}</p>
  </div>
</template>
