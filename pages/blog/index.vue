<script setup>
const { data: posts } = await useAsyncData('posts', () =>
  queryContent('/blog').find()
)
</script>

<template>
  <div class="border pb-8 rounded bg-gray-100 p-6 mt-8">
  <h1 class="text-3xl my-8 font-bold ">Blog Posts</h1>
<p class="font-medium max-w-4xl">

  I like to write about anything thta I am currently working or something new that interests me. If you would like me to
  write about something or be a guest blogger on your blog please reach out to me on Twitter. If you would like to
  subscribe to an RSS feed you can find it here.
</p>

</div>
  <section class="grid md:grid-cols-3 mt-8 gap-10 mb-16">
    <Post :posts="posts" />
  </section>
</template>

