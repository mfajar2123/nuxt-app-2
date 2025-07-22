<template>
  <div>
    <h2>{{ post.title }}</h2>
    <ContentRenderer :value="post" />
  </div>
</template>

<script setup>
const route = useRoute();

const { data: post } = await useAsyncData("blog-post", () =>
  queryContent("blog")
    .where({ _path: `/blog/${route.params.slug}` })
    .findOne()
);
</script>
