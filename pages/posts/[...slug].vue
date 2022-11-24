<template>
  <div>
    <div
      class="mx-auto w-[90%] sm:w-[600px] md:w-[740px] lg:w-[980px] xl:w-[1250px] 2xl:w-[1500px] mt-10"
    >
      <NuxtLink class="font-bold text-2xl md:text-4xl" to="/">
        <span class="hover:underline">Blog</span>.
      </NuxtLink>
      <div class="mt-20">
        <p
          id="post_title"
          class="text-[44px] md:text-7xl text-center md:text-start lg:text-[100px] leading-[53px] xl:leading-[100px] font-bold"
        >
          {{ post.title }}
        </p>
        <div class="flex flex-col-reverse md:flex md:flex-col">
          <div class="flex items-center gap-4 mt-7" id="author">
            <img
              alt="author_image"
              :src="post.author.picture"
              id="author_image"
              class="h-12 rounded-full"
            />
            <p id="author_name" class="font-bold text-xl">
              {{ post.author.name }}
            </p>
          </div>
          <img
            :src="post.ogImage.url"
            id="image_cover"
            alt="og_image"
            class="mt-12"
          />
        </div>
        <p
          class="w-[90%] md:w-[670px] md:mt-16 md:mx-auto text-lg font-normal mt-4"
        >
          {{ post.date }}
        </p>
      </div>
      <div
        class="mx-auto w-[90%] sm:w-[600px] md:w-[670px] xl:w-[680px] mt-8 lg:mt-14"
      >
        <ClientOnly>
          <ContentRenderer
            class="prose lg:prose-base prose-sm prose-slate pr-7 max-w-none"
            :value="post"
          />
        </ClientOnly>
      </div>
    </div>
  </div>
</template>

<script setup>
const slug = useRoute().params.slug.toString().replace(/,/g, "/");

const { data: post } = await useAsyncData(slug, () => {
  return queryContent(slug).findOne();
});

useHead({
  title: `${post.value.title}`,
});

console.log(post);
</script>
