<template>
  <section class="w-full">
    <h1 class="font-semibold text-center text-2xl mb-10">Resumen Noticias</h1>
    <NewsList :news="news" />
  </section>
</template>

<script>
export default {
  name: 'HomePage',
  async asyncData({ $content }) {
    const news = await $content('/news')
      .without(['body', 'toc'])
      .sortBy('date', 'desc')
      .limit(2)
      .fetch()
    return { news }
  },
}
</script>
