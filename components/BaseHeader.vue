<template>
  <header class="flex justify-between items-center h-24">
    <NuxtLink to="/">
      <NuxtLogo class="ml-6 w-20 h-20" />
    </NuxtLink>
    <div class="mr-12">
      <NuxtLink class="link" to="/news">News</NuxtLink>
      <NuxtLink class="link" to="/about">About</NuxtLink>
    </div>
  </header>
</template>

<script>
export default {
  name: 'BaseHeader',
}
</script>

<style scoped>
.link.nuxt-link-active {
  @apply text-green-500;
}
.link:hover {
  transition: 0.3s;
  @apply text-green-300;
}
</style>
