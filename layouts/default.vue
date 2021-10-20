<template>
  <div>
    <BaseHeader />
    <main class="min-h-screen bg-gray-100 pt-10">
      <Nuxt />
    </main>
  </div>
</template>

<script>
import BaseHeader from '~/components/BaseHeader.vue'

export default {
  components: {
    BaseHeader,
  },
}
</script>
