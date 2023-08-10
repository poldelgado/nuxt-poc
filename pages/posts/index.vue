<script setup>

const { data: posts } = await useFetch('https://jsonplaceholder.typicode.com/posts')

</script>
<template>
    <h1 class="">POSTS PAGE</h1>
    <section>
        <ul>
            <li v-for="{title, id} in posts" :key="id">{{ title }}</li>
        </ul>
    </section>
</template>