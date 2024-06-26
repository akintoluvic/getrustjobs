<script setup lang="ts">
import type { JobType } from '#build/layouts/default.vue';

const route = useRoute();

const featuredJobs = useState<JobType[]>("featured");
const allJobs = useState<JobType[]>("all-jobs");

const filterExactJob = () => {
  let jobArray =
    route.query === "featured" ? featuredJobs.value : allJobs.value;
  return jobArray.filter(
    (job) => job.slug.split("?")[0] === route.params.job
  )[0];
};

const jobDetails = filterExactJob();
</script>
<template>
  <GeneralSectionWrapper :title="jobDetails.jobTitle" :description="'at ' + jobDetails.companyName"
    background-color="bg-white">
    <div class="mt-12 min-h-96 grid md:grid-cols-3 gap-6">
      <div
        class="md:col-span-2 rounded-3xl border border-gray-100 bg-white hover:bg-white/60 hover:border-gray-200 p-2 shadow-2xl shadow-gray-600/10">
        <div class="relative gap-6 flex flex-col sm:flex-row">
          <div
            class="flex rounded-2xl border-2 border-gray-100 overflow-hidden py-4 sm:py-0 sm:w-1/3 md:w-2/5 lg:w-1/3">
            <img class="m-auto w-auto h-24 rounded-xl" :src="jobDetails.logo" loading="lazy" alt="company logo" />
          </div>
          <div class="mt-6 mb-2 px-6 sm:px-0 space-y-6 sm:w-2/3 md:w-3/5 lg:w-2/3">
            <div class="">
              <h2 class="text-xl font-semibold text-gray-800">
                {{ jobDetails.jobTitle }}
              </h2>
              <p class="mt-2 text-gray-600">{{ jobDetails.companyName }}</p>
              <div class="flex gap-4 sm:gap-6 flex-wrap my-4">
                <div v-for="(tag, index) in jobDetails.tags" :key="tag"
                  class="relative flex items-center before:absolute before:inset-y-0 before:-left-0.5 before:my-auto before:h-1 before:w-1 before:rounded-full"
                  :class="[
                    index % 2 === 0
                      ? 'before:bg-green-400'
                      : 'before:bg-red-400',
                  ]">
                  <span class="rounded-full border px-2.5 py-1 text-sm tracking-wider" :class="[
                    index % 2 === 0
                      ? 'border-green-100 bg-green-50 text-green-900'
                      : 'border-red-100 bg-red-50 text-red-900',
                  ]">{{ tag }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="h-[1px] bg-gray-100 mx-4 mt-6"></div>

        <!-- <div class=""> ahdjfidf</div> -->

        <div class="p-5">
          <div>
            <div id="salary" class="py-5">
              <h2 class="text-4xl font-bold">Job description</h2>
              <p class="py-4">
                Job details are listed on the companies website regarding this
                job. Click on the APPLY button to see more information.
              </p>
            </div>
            <div id="salary" class="py-5">
              <h2 class="text-4xl font-bold">Salary and compensation</h2>
              <p class="py-4">
                Salary details are listed on the companies website regarding
                this job. Click on the APPLY button to see more information.
              </p>
            </div>
            <div id="benefits" class="py-5">
              <h2 class="text-4xl font-bold">Benefits</h2>
              <ul>
                <p class="py-4">Click on APPLY to view more benefits</p>
                <!--[--><!--]-->
              </ul>
            </div>
          </div>
          <div class="rounded-xl border w-full border-solid border-gray-300 p-5 mt-20 mb-5">
            <div class="w-full">
              <a :href="jobDetails.applyUrl"
                class="px-3 flex justify-center py-3 bg-red-600 text-white w-full rounded-lg"><span>Apply for this
                  job</span></a>
            </div>
            <p class="font-bold text-center text-sm py-4">
              👉 Please reference you found the job on GetRustJobs, this helps
              us get more companies to post here, thanks!
            </p>
            <p class="text-sm text-center">
              When applying for jobs, you should NEVER have to pay to apply. You
              should also NEVER have to pay to buy equipment which they then pay
              you back for later. Also never pay for trainings you have to do.
              Those are scams! NEVER PAY FOR ANYTHING! Posts that link to pages
              with "how to work online" are also scams. Don't use them or pay
              for them. Also always verify you're actually talking to the
              company in the job post and not an imposter. A good idea is to
              check the domain name for the site/email and see if it's the
              actual company's main domain name. Scams in remote work are
              rampant, be careful! Read more to avoid scams. When clicking on
              the button to apply above, you will leave GetRustJobs and go to
              the job application page for that company outside this site.
              GetRustJobs accepts no liability or responsibility as a
              consequence of any reliance upon information on there (external
              sites) or here.
            </p>
          </div>
        </div>
      </div>

      <div class="flex flex-col gap-6">
        <div
          class="grid place-items-center w-full rounded-3xl border border-gray-100 bg-white hover:bg-white/60 hover:border-gray-200 p-10 shadow-2xl shadow-gray-600/10">
          <picture
            class="flex overflow-hidden grow-0 shrink-0 justify-center items-center rounded-full border border-solid border-inherit h-40 w-40 text-base tracking-wider text-black bg-white">
            <img src="https://startup.jobs/logos/21791" alt="Backbase" width="48" height="48"
              class="object-cover w-full h-full rounded-full" />
          </picture>
          <div class="py-4 text-center">
            <h4 class="text-2xl font-black">{{ jobDetails.companyName }}</h4>
            <a href="" class="underline text-xl w-full font-bold">
              <p class="w-full"></p>
            </a>
          </div>
          <div class="py-2 w-full">
            <a :href="jobDetails.applyUrl"><button class="px-3 py-2 bg-red-600 rounded-lg text-white w-full">
                <span> Apply Now </span>
              </button></a>
          </div>
        </div>
        <div
          class="grid place-items-center w-full h-80 rounded-3xl border border-gray-100 bg-white hover:bg-white/60 hover:border-gray-200 p-2 shadow-2xl shadow-gray-600/10">
          <span class="grid place-items-center w-full max-h-80 h-full">Advertise here</span>
        </div>
      </div>
    </div>
  </GeneralSectionWrapper>
</template>
