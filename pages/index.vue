<template>
  <div class="home">
    <main>
      <Hero />
      <div
        class="mt-16 grid place-content-center place-items-center lg:place-items-start gap-8 lg:gap-16 xl:gap-24"
      >
        <ArticleCard :post-data="postData" />
      </div>
    </main>
  </div>
</template>

<script setup>
const postData = await queryContent("/post").where({ _partial: false }).find();

console.log(postData);

useHead({
  title: "Nuxt Blog Example with Markdown",
});
</script>
