<template>
  <section class="w-full pb-14">
    <h1 class="font-semibold text-center text-2xl mb-10">Noticias</h1>
    <NewsList :news="news" />
  </section>
</template>

<script>
export default {
  name: 'NewsPage',
  async asyncData({ $content }) {
    const news = await $content('/news')
      .without(['body', 'toc'])
      .sortBy('date', 'desc')
      .fetch()
    return { news }
  },
}
</script>
