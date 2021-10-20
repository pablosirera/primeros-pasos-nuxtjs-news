<template>
  <article class="mb-20 w-full max-w-3xl mx-auto">
    <h1 class="text-4xl">{{ doc.title }}</h1>
    <nuxt-content :document="doc" />
  </article>
</template>

<script>
export default {
  name: 'NewsDetail',
  async asyncData({ $content, params }) {
    const doc = await $content(`/news/${params.slug}`).fetch()
    return { doc }
  },
}
</script>
