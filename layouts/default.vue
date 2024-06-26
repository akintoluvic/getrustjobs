<script setup lang="ts">

export type JobType = {
  logo: string
  companyName: string
  jobTitle: string
  slug: string
  tags: string[]
  applyUrl: string
}

const featuredJobs = useState<JobType[]>('featured', () => [
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'TransferGo',
    jobTitle: 'Backend Engineer - Cards & Integrations',
    slug: '232321?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '2329721?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '232867721?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'TransferGo',
    jobTitle: 'Backend Engineer - Cards & Integrations',
    slug: '2321?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '232978?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '2328921?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'TransferGo',
    jobTitle: 'Backend Engineer - Cards & Integrations',
    slug: '232kmjid?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'PoMedia Hubrisre',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '23297d21?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubrisa',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '2328677a21?type=featured',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
])

const allJobs = useState<JobType[]>('all-jobs', () => [
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'TransferGo',
    jobTitle: 'Backend Engineer - Cards & Integrations',
    slug: '232321',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '2329721',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '232867721',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'TransferGo',
    jobTitle: 'Backend Engineer - Cards & Integrations',
    slug: '2321',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '232978',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubris',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '2328921',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'TransferGo',
    jobTitle: 'Backend Engineer - Cards & Integrations',
    slug: '232kmjid',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'PoMedia Hubrisre',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '23297d21',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },
  {
    logo: 'https://startup.jobs/logos/21791',
    companyName: 'GoMedia Hubrisa',
    jobTitle: 'Backend Engineer Infra sys',
    slug: '2328677a21',
    tags: ['Remote', 'Fadgure', 'Fulltime'],
    applyUrl:'https://startup.jobs/backend-engineer-backbase-5546703'
  },

])
</script>
<template>
  <div>
    <GeneralNavbar />
    <slot />
    <!-- <AppFooter /> -->
  </div>
</template>
