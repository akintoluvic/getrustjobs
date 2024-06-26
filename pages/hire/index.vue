<script setup lang="ts">
import { ToggleGroup, ToggleGroupItem } from '@/components/ui/toggle-group'

const filters = ref([])
</script>
<template>
  <GeneralSectionWrapper
    title="Top Rust Engineers"
    description="Hire the hottest and topmost engineers with experience from leading companies."
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
    <div class="grid sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <GeneralEngineerCard slug="/hire/233" />
      <GeneralEngineerCard slug="/hire/233" />
      <GeneralEngineerCard slug="/hire/233" />
      <GeneralEngineerCard slug="/hire/233" />
      <GeneralEngineerCard slug="/hire/233" />
      <GeneralEngineerCard slug="/hire/233" />
    </div>
  </GeneralSectionWrapper>
</template>