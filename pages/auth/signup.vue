
<script setup lang="ts">
import { h } from 'vue'
import { useForm } from 'vee-validate'
import { toTypedSchema } from '@vee-validate/zod'
import * as z from 'zod'
import { vAutoAnimate } from '@formkit/auto-animate/vue'

import { Button } from '@/components/ui/button'
import {
  FormControl,
  FormField,
  FormItem,
  FormLabel,
  FormMessage,
} from '@/components/ui/form'
import { Input } from '@/components/ui/input'
import { toast } from '@/components/ui/toast'

const formSchema = toTypedSchema(z.object({
  email: z.string().min(2).max(50),
  password: z.string().min(2).max(50),
  confirmPassword: z.string().min(2).max(50),
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
    title="Sign up to create your profile"
    description="Access the bext and highest talents from around the globe."
    background-color="bg-white"
    class="max-w-3xl mx-auto"
  >
    <div
      class="rounded-3xl max-w-xl mx-auto mt-12 border border-gray-100 bg-white p-2 shadow-2xl shadow-gray-600/10"
    >
      <div class="gap-6 grid p-16">
        <h3 class="text-2xl font-medium text-center mb-4">Enter details below</h3>
        <form class="space-y-6" @submit="onSubmit">
          <FormField v-slot="{ componentField }" name="email" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Email</FormLabel>
              <FormControl>
                <Input type="email" placeholder="Email" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="password" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Password</FormLabel>
              <FormControl>
                <Input type="password" placeholder="Password" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          <FormField v-slot="{ componentField }" name="confirmPassword" :validate-on-blur="!isFieldDirty">
            <FormItem v-auto-animate>
              <FormLabel>Confirm Password</FormLabel>
              <FormControl>
                <Input type="password" placeholder="Confirm Password" v-bind="componentField" />
              </FormControl>
              <FormMessage />
            </FormItem>
          </FormField>
          
          <Button type="submit" class="w-full">
            Submit
          </Button>

          <div class="text-center text-sm">
            Already have an account?
            <NuxtLink to="/auth" class="underline">
              Sign in
            </NuxtLink>
          </div>
        </form>
      </div>
    </div>
  </GeneralSectionWrapper>
  
</template>