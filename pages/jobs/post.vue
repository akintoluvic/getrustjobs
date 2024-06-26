<script setup lang="ts">
import { h } from 'vue'
import { useForm } from 'vee-validate'
import { toTypedSchema } from '@vee-validate/zod'
import * as z from 'zod'
import { vAutoAnimate } from '@formkit/auto-animate/vue'

import { Button } from '@/components/ui/button'
import {
  FormControl,
  FormDescription,
  FormField,
  FormItem,
  FormLabel,
  FormMessage,
} from '@/components/ui/form'
import { Input } from '@/components/ui/input'
import { Textarea } from '@/components/ui/textarea'
import { toast } from '@/components/ui/toast'

const formSchema = toTypedSchema(z.object({
  companyName: z.string().min(2).max(50),
  companyUrl: z.string().min(2).max(50),
  companyEmail: z.string().min(2).max(50),
  companyPhone: z.string().min(2).max(50),
  jobTitle: z.string().min(2).max(50),
  aboutCompany: z.string().min(2).max(50),
  description: z.string().min(2).max(50),
}))

const { isFieldDirty, handleSubmit } = useForm({
  validationSchema: formSchema,
})

const onSubmit = handleSubmit((values) => {
  toast({
    title: 'You submitted the following values:',
    description: h('pre', { class: 'mt-2 w-[340px] rounded-md bg-slate-950 p-4' }, h('code', { class: 'text-white' }, JSON.stringify(values, null, 2))),
  })
})
</script>
<template>
  <GeneralSectionWrapper
    title="Post your job openings"
    description="Access the bext and highest talents from around the globe."
    background-color="bg-white"
    class="max-w-3xl mx-auto"
  >
    <div
      class="rounded-3xl mt-12 border border-gray-100 bg-white p-2 shadow-2xl shadow-gray-600/10"
    >
      <div class="gap-6 grid p-16">
        <h3 class="text-2xl font-medium text-center mb-4">Add Job details below</h3>
        <form class="space-y-6" @submit="onSubmit">
          <FormField v-slot="{ componentField }" name="companyName" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Company Name</FormLabel>
              <FormControl>
                <Input type="text" placeholder="Company Name" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="companyEmail" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Company Email</FormLabel>
              <FormControl>
                <Input type="text" placeholder="Company Email" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="companyUrl" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Company Website</FormLabel>
              <FormControl>
                <Input type="text" placeholder="www.company.com" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="companyPhone" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Company Phone</FormLabel>
              <FormControl>
                <Input type="text" placeholder="(+56) 8627 3738 22" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="jobTitle" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Job Title</FormLabel>
              <FormControl>
                <Input type="text" placeholder="Backend Developer" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="aboutCompany" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>About Company</FormLabel>
              <FormControl>
                <Textarea placeholder="About Company" v-bind="componentField" />
              </FormControl>
              <FormDescription>
                This is your public display name.
              </FormDescription>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="description" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Job description</FormLabel>
              <FormControl>
                <Textarea placeholder="Type Job description here." v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <Button type="submit" class="w-full">
            Submit
          </Button>
        </form>
      </div>
    </div>
  </GeneralSectionWrapper>
  
</template>