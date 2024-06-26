<script setup lang="ts">
import type { JobType } from '#build/layouts/default.vue';
import { ToggleGroup, ToggleGroupItem } from '@/components/ui/toggle-group'

const allJobs = useState<JobType[]>("all-jobs");
  const filters = ref([])
</script>
<template>
  <GeneralSectionWrapper
    title="Rust Jobs for You"
    description="Access the hottest and highest paying jobs from your favorite tech companies."
    background-color="bg-white"
  >
    <div class="my-12 flex gap-6 justify-center items-center">
      <div>Apply filters:</div>
      <ToggleGroup v-model="filters" class="flex gap-4" type="multiple" size="lg">
        <ToggleGroupItem class="border rounded-full" value="bold" aria-label="Toggle bold">
          Backend
        </ToggleGroupItem>
        <ToggleGroupItem class="border rounded-full" value="italic" aria-label="Toggle italic">
          Industrial
        </ToggleGroupItem>
        <ToggleGroupItem class="border rounded-full" value="underline" aria-label="Toggle underline">
          Why
        </ToggleGroupItem>
      </ToggleGroup>
    </div>
    <div class="flex flex-col gap-6">
      <GeneralJobCard 
        v-for="job in allJobs" 
        :key="job.slug"
        :logo="job.logo"
        :companyName="job.companyName"
        :jobTitle="job.jobTitle"
        :slug="job.slug"
        :tags="job.tags"
      />
      
    </div>
  </GeneralSectionWrapper>
</template>