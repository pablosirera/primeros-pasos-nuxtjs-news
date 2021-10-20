<template>
  <div class="grid grid-cols-2 gap-4 px-4">
    <NewsCard
      v-for="currentNew in news"
      :key="currentNew.path"
      :card-info="currentNew"
    />
  </div>
</template>

<script>
import NewsCard from '~/components/NewsCard.vue'

export default {
  name: 'NewsList',
  components: {
    NewsCard,
  },
  props: {
    news: {
      type: Array,
      default: () => [],
    },
  },
}
</script>
