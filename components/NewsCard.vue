<template>
  <div
    class="shadow-xl bg-white rounded cursor-pointer hover:shadow-2xl"
    @click="goToDetail()"
  >
    <img :src="cardInfo.img" class="h-64 w-full object-cover" />
    <div class="p-4">
      <h2>{{ cardInfo.title }}</h2>
      <p>{{ cardInfo.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewsCard',
  props: {
    cardInfo: {
      type: Object,
      default: () => ({}),
    },
  },
  methods: {
    goToDetail() {
      this.$router.push({ path: this.cardInfo.path })
    },
  },
}
</script>
