<script setup lang="ts">
  defineProps<{
    title: string
    description: string
    backgroundColor?: string
  }>()
</script>

<template>
  <section 
    class="py-32"
    :class="[ backgroundColor ? backgroundColor : 'bg-gray-50' ]"
  >
    <div class="mx-auto px-4 sm:px-12 xl:max-w-6xl xl:px-0">
      <div class="text-center">
        <h2 class="text-3xl font-bold text-gray-800 md:text-4xl xl:text-5xl">{{ title }}</h2>
        <p class="mx-auto mt-6 text-gray-700 md:w-3/4 lg:w-3/5">
          {{ description }}
        </p>
      </div>
      <slot />
    </div>
  </section>
</template>