<script setup lang="ts">

import type { JobType } from '@/layouts/default.vue';

const featuredJobs = useState<JobType[]>("featured");

const trustedCompanies = [
  {
    name: 'airbnb',
    logo: 'https://res.cloudinary.com/pitch-software/image/upload/website/pricing/logos/linear.svg'
  },
  {
    name: 'bissell',
    logo: 'https://res.cloudinary.com/pitch-software/image/upload/website/pricing/logos/synthesia.svg'
  },
  {
    name: 'primer',
    logo: 'https://res.cloudinary.com/pitch-software/image/upload/website/pricing/logos/primer.svg'
  },
  {
    name: 'dept',
    logo: 'https://res.cloudinary.com/pitch-software/image/upload/website/pricing/logos/dept_vlvpvs.svg'
  },
  {
    name: 'koto',
    logo: 'https://res.cloudinary.com/pitch-software/image/upload/website/pricing/logos/koto.svg'
  },
  {
    name: 'synthesia',
    logo: 'https://res.cloudinary.com/pitch-software/image/upload/website/pricing/logos/synthesia.svg'
  },
]

</script>
<template>
  <div class="">
    <!-- Header -->
    <header class="relative pt-24 sm:pt-28 md:pt-32 lg:pt-36">
      <svg class="absolute top-0" width="1635" height="1117" viewBox="0 0 1635 1117" fill="none" xmlns="http://www.w3.org/2000/svg">
        <g opacity="0.6">
          <g filter="url(#filter0_f_214_7)">
            <rect x="542.233" y="146" width="284.361" height="284.361" transform="rotate(30.0124 542.233 146)"
              fill="#001AFF" />
          </g>
          <g filter="url(#filter1_f_214_7)">
            <circle cx="1032.85" cy="396.64" r="201.5" fill="#00C2FF" />
          </g>
          <g filter="url(#filter2_f_214_7)">
            <path
              d="M702.852 272.14L768.522 474.252H981.036L809.109 599.165L874.779 801.277L702.852 676.365L530.925 801.277L596.595 599.165L424.668 474.252H637.182L702.852 272.14Z"
              fill="#DB00FF" />
          </g>
          <g filter="url(#filter3_f_214_7)">
            <path d="M1129.56 479.845L1112.73 861.155L790.916 655.925L1129.56 479.845Z" fill="#00FFA3" />
          </g>
        </g>
        <defs>
          <filter id="filter0_f_214_7" x="0" y="-254" width="1188.47" height="1188.47" filterUnits="userSpaceOnUse"
            color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix" />
            <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
            <feGaussianBlur stdDeviation="200" result="effect1_foregroundBlur_214_7" />
          </filter>
          <filter id="filter1_f_214_7" x="431.352" y="-204.86" width="1203" height="1203" filterUnits="userSpaceOnUse"
            color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix" />
            <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
            <feGaussianBlur stdDeviation="200" result="effect1_foregroundBlur_214_7" />
          </filter>
          <filter id="filter2_f_214_7" x="24.668" y="-127.86" width="1356.37" height="1329.14"
            filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix" />
            <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
            <feGaussianBlur stdDeviation="200" result="effect1_foregroundBlur_214_7" />
          </filter>
          <filter id="filter3_f_214_7" x="390.917" y="79.845" width="1138.64" height="1181.31"
            filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix" />
            <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
            <feGaussianBlur stdDeviation="200" result="effect1_foregroundBlur_214_7" />
          </filter>
        </defs>
      </svg>

      <div class="mx-auto px-4 sm:px-12 xl:max-w-7xl xl:px-0">
        <div class="relative z-10 text-center md:mx-auto md:w-5/6 lg:w-4/6">
          <h1 class="relative text-cente text-5xl font-bold text-gray-900 dark:text-white sm:text-5xl md:text-7xl">
            Get <span class=" text-red-900">Rust jobs</span> tailored <br class="hidde" />
            just for you.
            <span class="relative">
              <!-- <svg class="absolute inset-x-0 -bottom-1 w-full opacity-50" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 260 15.6">
                                    <path class="fill-[#957fef]" d="M206.8 7.3l-.1.3c.1-.2.2-.3.1-.3zM234.7 10h-.1c-.2.4-.1.3.1 0zM54.8 4.2l-.6-.4c.2.4.4.5.6.4zM17.1 5.1zM34.5 9.6l.1.3c0-.2 0-.3-.1-.3zM22.4 10.8c-.3-.1-.7-.1-1-.1.2.1.7.1 1 .1zM17.5 5c-.1.1-.2.1-.4.2.2-.1.3-.2.4-.2zM52.7 9.8l.5.9c-.1-.3-.3-.6-.5-.9zM19.5 11.6c-.2-.2-.4-.2-.6-.3 0 .2.3.3.6.3zM120.9 11.4c-.1.1-.2.2-.2.3.3-.1.3-.2.2-.3zM80.9 10.4h-.1s.1.1.2.1l-.1-.1zM92.6 10.4l-.2.2c.2-.1.2-.1.2-.2zM72.1 11.3c-.1.1-.3.2-.4.3l.4-.3z"></path>
                                    <path class="fill-[#957fef]" d="M260 6c-1-.6-4.7-1.2-5.8.3-.2-.1.1-.3.2-.4-.9.2-2.2.1-3.6 0s-2.9-.2-4.2 0c-1 1.5-3.9-.6-4.8 1.4l.5-.4c.9.5-1.2 1.4-1.5 1.9-.8-1.2-.1-1-1-2l1.1.4-.3-1c-3.1 2.8-6.2-.9-8.2 1.1.1-.1.1-.3.2-.4-1.4-.5-2.3.8-3.3 1.2-.1-.5.6-.9 1.1-1.3-2.4-.3-6.4 1.2-9 .4-.9.7.4.9-.6 1.5-.8-.2-1.4-.7-.4-1.1-2.3-1.2-7.6 1-11.1-.2-1.8.8-.7 1.1-3.5 1.6.7-.5-.7-1.7 1-1.7l.2-.5c-2.8-.1-6.6-.3-8.1 1.2-.1-1.1-.5-.2-1.6-.8-.4.1 0 .2.2.2-1 .9-1.6-.1-2.3.1l.3-.2-2 .7c-.3-.2-.8-.4-.9-.7v.8c-1.1 0-.5-1-1.9-.8l.3.6c-.9-.4-2.2.4-2.4-.5 0-.2.1-.1.4-.1-1.3-1.2-3.5.3-5.1-.3l.4 1.3c-1.6.4-1-.3-.9-.7-1.1 0-1.3-.4-2.7-.6-.7.3-.4.5-.6.8l-1.5-.4 1-.7c-2.3 1.8-5.6-.4-7.2 1.2-.8-.4.8-.7.3-1-2.6-.9-6 1-8.2 0-3.6-1-7.8-.4-11.8-1.1l.1.3-2.9-.4c-.8.7-2.7.3-4 1.1.1-.3-.1-.7.2-.9-1.2.1-2.6.4-3.3-.1l.4-.3c-2.7-.3-6.4-.5-7.9.1-.9 0-.9-.6-1.1-1-1.6-.1-2.6.2-3.9.7-.3-.2-.7-.3-1-.6l-.6.8c-.6-.1-.1-.7-.6-.9-2.5.9-5.3-.1-7-.1l.2.4c-.7.3-2.1-.3-1.2-.7-3.4-.6-5.1 1.2-9.6.8-.6-1.5-4.1.3-4.8-1.4-1.9.4-3.2-.3-4.5.6 0-.2-.2-.2.1-.3-.8-.6-3.3-.2-5.3.2l-.1-.5c-.9 1.2-4.2.9-4.9 2-.2-.2.4-.5.7-.7-1-1.1-1.8.5-3.1.2.1-.3-.3-.6 0-.8-4.4-1.2-10.6.7-16.3-.1-1.6 0 .6 1.2-1.5 1.1-.6-.6 1-1.1-.3-1.4-.9.7-1.3.5-2.6.5.2-.4 0-.6.9-.9-.7-.5-3.1.9-4.5 0 .1.3-.2.5-.5.7-2.1 1-4.9-.9-5.1-.4 0 0-.7.2-.1.3-.8 0-1.9-.2-1.7-.7-.4.3-.8.8-1.4.8l.3-.6c-.4.1-.8.5-1.1.6l.6.4c-.9-.5-2.6.8-2.6-.4h.3l-1.7-.5c-.7.5-1.3 1-2.5.9-.5-1.3-2.9-.2-4.3-.3l.1-.4c-1.1.6-4 .4-3.5.6-1.1 0-2.6-.2-2-.6-.8.1-2.7.1-3.2.9l-1.8-1c-1 1.6-3.6-.5-3.6 1.2-1-.2-.8-.6-1.5-.9-1.4.9-2.8.8-4.2.7v-.2c-1.4-.1-3.1.8-5.1 1l-.5-1.2c-1 .2-1.3 1.2-2.3 1-.2-.2 0-.3.2-.3-1 .3-2.3.1-3.1-.2-1.5 1-2.7.7-3.9 1.8-1.3-1 1.7-.6.6-1.6-2.2-.4-4.4.4-6.7 1.1-.2-.2 0-.4.1-.7 0 0-1.2.9-2.2 1.8C.9 8.3 0 9.4.5 10c-.5.9-1.2 1.4.9 2 .6-.5 2.5-1.3 2.9-.4l.1-.9c2.6-.6.4 1.8 3.6 1.6l-.7-.3c.6-.1 1.1-.7 1.8-.5.2.2-.2.4-.5.6.9-.5 1.7-.9 2.6-1.4.1.5.1.8-.4 1.2 2.5-.2-.6-1.6 2.4-1.4.6.4-.2.6-.5.9 1.4.7 2.3-.1 3.8-.6.1.8-.9.7.3 1.2-.3-.4-.5-1.1.5-1.2-.4.8.7.4 1.6.5-.2-.3-.1-.6.2-.8.4-.1.8.1 1.4.1l-1.1-.7c1.5-.8 2.4.3 3.6.6-.1.1-.3.3-.5.3 1.2.3 2.5.9 4.1.1l-.3.1c2.9-.9-1-1.3 2.4-2.2 1.1.1-.4 2.6 2.1 1.6-1.3-.6 1.6-1.7 3.1-2L32.4 10c.6 0 1.6-.5 2-.3l-.1-.3c-.2-1.3 1.9.1 3-.7-1.3 1.8-1.4 1.5-1.6 3.2 1-1 2.2-1.9 4.1-1.8l-1.5 1.4c2.5.2 5.5-1.9 7.6-3-.5 1 .3 1.4-.6 2.2l2.4-.3-.7 1.1c1-1.2 2.1-.4 1.9-1.9-.3.2-.2.4-.7.3.1-.4.5-1.4 1.7-1.3.9.3-.5.6-.2 1 .8-.6.9.3 1.7-.1l-.8-.6c.6-.9 1.4-.1 2.2-.5-1 .4-.7.9-.3 1.4l-.1-.1c.8-.1 1.6-.7 2-.2l-.5 1.2.9-.9c.3.1.6.6 0 .8 2.8.7-.1-2.5 3.6-1.5 0 .5-.4.8-1.4.5-.2.7.1 1.1 1.1 1.4v.1c1.9 0 4.4 0 5.6-.8.4.3 0 .6-.4.9 2.1.4 2.8-.7 5 .1l-1-.4c1.4-.6 4-.8 5.3.1l-.4.3c1.3-.7 3.5.6 4 0-.6-.4 0-.6-.8-1l3.4-.7.2 1.2 1.8-.4c-.4-.5 2.4.4 2.5-.7 1 .4-.4.9-.8 1.4 1-.3 1.1.2 2.1-.5l1 1.1 2.6-.7c-.1.1 0 .2-.1.3 1.2-.9 3.1.6 4.6-.9-.1.1-.1.1-.1.2.9-.8 2.9-.2 3.7 0 1.4-.2.6-1 .6-1.4 3.9.4 2.7.3 6-.9 2 1.4-2.4 2.1.1 3 .4-.6 2.1-1.1 4.1-1.3 1.8.5 4.8.9 6.5 1.9l-.2-.9 2.6-.4-1.5 1.2c.4-.3 1.7-.8 2.6-1.2 2.7-.7 1.4 1.9 3.5.7.1.1.1.2.2.3.7-.6 2.4-.3 4.4-.5l-.7 1.1-1.3-.3c.7 1.1 2.1-.1 3.4 0 1.3-.3.7-1.3 1.4-1.6.5.1 1.2-.2 1.6.1 1.1.4.1 1.3-.3 1.8 1-1.1 1.4-.9 3.6-1.3.1.5-.1.8-.4.9.5-.1.9-.3 1.2-.8l.7.7c2.5 1 2.6-2 5.6-1.5-.8.6 2.6 0 3.5.7-1.1.1.4 1.6-.2 2.3 2.4.5 1-1.3 3-1.4l-.9 1.3c1.9-.5.5-.7 2.4-1.1-.5.4.8.4-.3.8 2.5.2 1.9.1 4.1.3l.2-1.3c.7-.1 1 .5 1.2.7-.3 0-.8-.1-.7.1.8 1.2 1.4-.6 2.4.5-.2-.4-.5-1 .4-1.1-.3.8 1.4.8 1.4 1.2-.6-.6 2-.2 2.1-1 1 .7-.4.6-.4 1.1.9-1 3.7 0 4.6-.6 0 .1.1.1.1.2 1.2-.6 3-.7 5.3-1.5l-.8.7c2.2.4 1.4-1.5 3.3-1.5-.4 1.1 3.1 0 2.2 1.2 1.1-.6 2.3-.8 3.1-1.7 1 .6-2.1 1.4-.6 1.8l1.6-.5.3.6c.1-.4 1.5-.4 1.4-.8.2.7.9 1.2.8 1.8 1-.2 2.4.5 3.3-.1l.1.3c1-1.3 3.1-.2 3.6-1.5l.6.7c1.5-.1 1.3-1.5 2-1.8.6 0 1.4-.2 2 0-2 .8 1 1.1 1.4 1.6.8 0 3.1 0 3.7-.7-1 .7-.4 1.2-2.1 1.3.9 1.3 2.6-.2 4.5-.1v.6c2.7-.4 2.8-1.5 4-2.5.3.8.1 1-.7 1.7 1.8.5 4.7-.1 6.7 0 .6.5.2.9-.5 1.1 2.1-.6 4.7.1 6-1.2-.5.5.9.3 1.6.6 0-.3.1-.6.2-.6 1.3-.6 4.1-1.1 5.6-.7l-.5.4c1.7.1 3-.5 4.3-.9 1.3-.4 2.6-.8 4.5-.4.7.3-.7 1.1.7 1 .7-.5.4-1.5 2.2-1.3l-.1.9 1.2-.9c-.7-.7-2.6-.4-1.3-1.2 1.6.8 1.3-.9 3.3 0-.4.1-1 .8-1.3 1.2 2 .4 3.4.1 4.8-.1 1.4-.3 2.8-.6 4.9-.2 2-.8 4.6-1.2 5.9-1.9 0 .9 0 1.7-.8 2.4 1.8 0 2.4-2.1 3.7-.9.7-1.3 4.7-1.2 5-3l2-.8z"></path>
                                    <path class="fill-[#957fef]" d="M58.1 11.1c-1 0-1.9 0-2.3.2.2.2 2.3.6 2.3-.2zM208.2 13.3c-.1 0-.3.1-.4.1.1 0 .3 0 .4-.1zM216.3 12.9c-.1-.1-.2-.2-.4-.3 0 .3.1.5.4.3zM132.6 11.5zM178.5 13.7c.7-.4 1-.7 1-1-.4.1-.7.3-1 1zM163 12.6c-.1.1-.2.1-.3.2.3-.1.3-.2.3-.2zM130.2 12c.7-.4 1.6-.3 2.4-.5-.7.2-1.9-.3-2.4.5zM226.1 11.4l-.7.6.8-.4zM218.6 12c-.3-.1-1.7.3-1.3.6.4-.3.9-.5 1.3-.6zM189.6 11.4l-.3.6.7-.5z"></path>
                                </svg> -->
              <!-- <span class="relative bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 bg-clip-text px-2 text-transparent">companies.</span> -->
            </span>
          </h1>
          <p class="mt-6 mx-auto text-gray-700 dark:text-gray-300 md:max-w-xl">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
          <span class="flex gap-7 justify-center mx-auto mt-10">
            <NuxtLink
              class="relative flex h-11 w-max items-center justify-center px-10 before:absolute before:inset-0 before:rounded-full before:bg-gray-800 before:transition-transform before:duration-300 active:duration-75 active:before:scale-95"
              to="/jobs">
              <span class="relative text-base font-semibold text-white">Find Rust Job</span>
            </NuxtLink>
            <NuxtLink
              class="relative flex h-11 w-max items-center justify-center px-10 before:border before:border-border before:absolute before:inset-0 before:rounded-full before:bg-muted before:transition-transform before:duration-300 active:duration-75 active:before:scale-95"
              to="/jobs">
              <span class="relative text-base font-semibold text-gray-900">Create Profile</span>
            </NuxtLink>
          </span>
        </div>
      </div>
    </header>
    <!-- Trusted by -->
    <section class="mt-36 xl:max-w-6xl mx-auto border- border-gray-100 py-8 text-center md:py-12">
      <span class="text-sm font-semibold tracking-wider text-gray-800" style="cursor: pointer;">
        TRUSTED BY
      </span>

      <div
        class="mt-8 flex flex-wrap justify-center gap-6 brightness-75 contrast-200 grayscale sm:justify-between lg:gap-24">
        <img v-for="company in trustedCompanies" :key="company.name" class="h-8 w-auto lg:h-10 lg:w-auto"
          :src="company.logo" loading="lazy" :alt="company.name">
      </div>
    </section>

    <!-- Rust Engineers -->
    <GeneralSectionWrapper title="Top Rust Engineers"
      description="Hire the hottest and topmost engineers with experience from leading companies.">
      <div class="mt-12 grid sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <GeneralEngineerCard slug="/hire/233" />
        <GeneralEngineerCard slug="/hire/234" />
        <GeneralEngineerCard slug="/hire/235" />
        <GeneralEngineerCard slug="/hire/245" />
        <GeneralEngineerCard slug="/hire/2393" />
      </div>
    </GeneralSectionWrapper>

    <!-- Featured Jobs -->
    <GeneralSectionWrapper title="Featured Jobs"
      description="Access the hottest and highest paying jobs from your favorite tech companies."
      background-color="bg-white">
      <div class="mt-12 flex flex-col gap-6">
        <GeneralJobCard v-for="job in featuredJobs" :key="job.slug" :logo="job.logo" :companyName="job.companyName"
          :jobTitle="job.jobTitle" :slug="job.slug" :tags="job.tags" />

      </div>
    </GeneralSectionWrapper>



    <h1>Welcome to the homepage</h1>
    <Button>Button</Button>
    <Badge variant="destructive"> Destructive </Badge>
  </div>
</template>
