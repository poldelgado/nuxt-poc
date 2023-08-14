<script setup>
const { data: posts } = await useFetch(
  "https://jsonplaceholder.typicode.com/posts"
);
</script>
<template>
  <h1 class="">POSTS PAGE</h1>
  <section>
    <div class="row">
      <article
        class="col-2 mb-3 d-flex align-items-stretch"
        v-for="{ title, id } in posts"
        :key="id"
      >
        <NuxtLink class="card-link" :to="`/posts/${id}`">
          <div class="card cards shadow" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">{{ title }}</h5>
              <h6 class="card-subtitle mb-2 text-body-secondary">
                Card subtitle
              </h6>
              <p class="card-text">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
              </p>
            </div>
          </div>
        </NuxtLink>
      </article>
    </div>
  </section>
</template>

<style scoped>
.cards {
  transition: all 0.9s ease;
  cursor: pointer;
}
.cards:hover {
  box-shadow: 5px 6px 6px 2px #e9ecef;
  transform: scale(1.05);
}
</style>
