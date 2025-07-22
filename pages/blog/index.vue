<template>
  <div>
    <li v-for="post in posts" :key="post._path">
      <NuxtLink :to="post._path">{{ post.title }}</NuxtLink>
    </li>
  </div>
</template>

<script setup>
const { data: posts } = await useAsyncData("blog-posts", () =>
  queryContent("blog").find()
);
</script>
