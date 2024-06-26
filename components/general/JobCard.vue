<script setup lang="ts">

  defineProps<{
    slug: string
    logo: string
    companyName: string
    jobTitle: string
    tags: string[]
  }>()
</script>
<template>
  <NuxtLink :to="'/jobs/' + slug">
    <div
      class="rounded-3xl border border-gray-100 bg-white hover:bg-white/60 hover:border-gray-200 p-2 shadow-2xl shadow-gray-600/10"
    >
      <div class="relative gap-6 flex flex-col sm:flex-row">
        <div
          class="flex rounded-2xl border-2 border-gray-100 overflow-hidden py-4 sm:py-0 sm:w-1/3 md:w-2/5 lg:w-1/3"
        >
          <img
            class="m-auto w-auto h-24 rounded-xl"
            :src="logo"
            loading="lazy"
            :alt="companyName + 'logo'"
          />
        </div>
        <div class="mt-6 mb-2 px-6 sm:px-0 space-y-6 sm:w-2/3 md:w-3/5 lg:w-2/3">
          <div class="">
            <h2 class="text-xl font-semibold text-gray-800">
              {{ jobTitle }}
            </h2>
            <p class="mt-2 text-gray-600">TransferGo</p>
            <div class="flex gap-4 sm:gap-6 flex-wrap my-4">
              <!-- <div
                v-for="tag in tags"
                :key="tag"
                class="relative flex items-center before:absolute before:inset-y-0 before:-left-0.5 before:my-auto before:h-1 before:w-1 before:rounded-full before:bg-green-400"
              >
                <span
                  class="rounded-full border  px-2.5 py-1 text-sm tracking-wider text-green-900"
                  >{{ tag }}</span
                >
              </div> -->
              <div
                v-for="(tag, index) in tags"
                :key="tag"
                class="relative flex items-center before:absolute before:inset-y-0 before:-left-0.5 before:my-auto before:h-1 before:w-1 before:rounded-full"
                :class="[index % 2 === 0 ? 'before:bg-green-400' : 'before:bg-red-400']"
              >
                <span
                  class="rounded-full border px-2.5 py-1 text-sm tracking-wider"
                  :class="[index % 2 === 0 ? 'border-green-100 bg-green-50 text-green-900' : 'border-red-100 bg-red-50 text-red-900']"
                  >{{ tag }}</span
                >
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </NuxtLink>
</template>
