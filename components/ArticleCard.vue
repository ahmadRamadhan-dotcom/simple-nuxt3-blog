<template>
  <div
    v-for="(data, index) in postData"
    :key="index"
    :class="
      index == 0
        ? 'w-[90%] sm:w-[600px] md:w-[740px] lg:w-[1000px] xl:w-[1250px] 2xl:w-[1500px] min-h-[10em] md:h-[46em] lg:h-[55em] 2xl:min-h-[62em] md:col-span-2 mb-9'
        : 'w-[90%] mb-14 sm:w-[600px] md:w-[340px] lg:w-[450px] xl:w-[570px] 2xl:w-[700px] min-h-[10em] md:min-h-[20em]'
    "
  >
    <NuxtLink :to="`/posts${data._path}`">
      <img id="cover_image" :src="data.coverImage" alt="" />
      <p
        id="title"
        :class="
          index == 0 ? 'block md:hidden text-4xl lg:text-4xl' : 'text-[30px]'
        "
        class="font-normal hover:underline mt-7"
      >
        {{ data.title }}
      </p>
    </NuxtLink>
    <div v-if="index == 0" class="md:grid md:grid-cols-2 md:gap-10 md:mt-10">
      <div class="">
        <NuxtLink
          :to="`/posts${data._path}`"
          id="title"
          class="hidden md:block hover:underline text-4xl xl:text-[44px] font-normal mt-7"
        >
          {{ data.title }}
        </NuxtLink>
        <p id="date" class="font-normal mt-5 text-lg">{{ data.date }}</p>
      </div>
      <div>
        <p id="short_desc" class="text-lg mt-5">
          {{ data.excerpt }}
        </p>
        <div id="author" class="flex items-center gap-4 mt-3">
          <img
            id="author_image"
            :src="data.author.picture"
            alt="author_image"
            class="h-12 rounded-full"
          />
          <p id="author_name" class="font-bold text-xl">
            {{ data.author.name }}
          </p>
        </div>
      </div>
    </div>
    <div v-else>
      <p id="date" class="font-normal mt-5 text-lg">{{ data.date }}</p>
      <p id="short_desc" class="text-lg mt-5">
        {{ data.excerpt }}
      </p>
      <div id="author" class="flex items-center gap-4 mt-3">
        <img
          id="author_image"
          :src="data.author.picture"
          alt="author_image"
          class="h-12 rounded-full"
        />
        <p id="author_name" class="font-bold text-xl">
          {{ data.author.name }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  postData: Array,
});
</script>
