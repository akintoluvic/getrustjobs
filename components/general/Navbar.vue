<template>
    <nav class="w-full">
        <div class="mx-auto px-4 sm:px-12 xl:max-w-7xl xl:px-0">
            <div class="relative flex flex-wrap items-center justify-between gap-6 lg:gap-0 lg:py-4">
                <div class="relative z-20 flex w-full justify-between md:px-0 lg:w-max">
                    <NuxtLink to="/" aria-label="logo" class="flex items-center space-x-2 text-2xl italic font-black">
                        GetRustJobs
                    </NuxtLink>

                    <button aria-label="humburger" id="hamburger" class="relative -mr-6 p-6 lg:hidden">
                        <div aria-hidden="true"
                            class="m-auto h-0.5 w-5 rounded bg-sky-900 transition duration-300 dark:bg-gray-300"></div>
                        <div aria-hidden="true"
                            class="m-auto mt-2 h-0.5 w-5 rounded bg-sky-900 transition duration-300 dark:bg-gray-300">
                        </div>
                    </button>
                </div>
                <div id="navlinks"
                    class="invisible absolute top-full left-0 z-20 w-full origin-top-right translate-y-1 scale-90 flex-col flex-wrap justify-end gap-6 rounded-3xl border p-8 opacity-0 transition-all duration-300 lg:visible lg:relative lg:flex lg:w-auto lg:translate-y-0 lg:scale-100 lg:flex-row lg:items-center lg:gap-0 lg:border-none lg:bg-transparent lg:p-0 lg:opacity-100 lg:shadow-none lg:peer-checked:translate-y-0 dark:lg:bg-transparent">
                    <div class="text-gray-600 dark:text-gray-300 lg:pr-4">
                        <ul class="space-y-6 text-base font-medium tracking-wide lg:flex lg:space-y-0 lg:text-sm">
                            <li>
                                <NuxtLink
                                    class="block transition hover:text-primary dark:hover:text-primaryLight md:px-4"
                                    to="/jobs">
                                    <span>Find job</span>
                                </NuxtLink>
                            </li>
                            <li>
                                <NuxtLink
                                    class="block transition hover:text-primary dark:hover:text-primaryLight md:px-4"
                                    to="/hire">
                                    <span>Hire engineers</span>
                                </NuxtLink>
                            </li>

                            <li>
                                <NuxtLink
                                    class="block transition hover:text-primary dark:hover:text-primaryLight md:px-4"
                                    to="/auth">
                                    <span>Manage profile</span>
                                </NuxtLink>
                            </li>
                        </ul>
                    </div>

                    <div
                        class="mt-12 -ml-1 flex w-full flex-col space-y-2 border-primary/10 dark:border-gray-700 sm:flex-row md:w-max lg:mt-0 lg:mr-6 lg:space-y-0 lg:border-l lg:pl-6">
                        <!-- <a class="relative ml-auto flex h-9 w-full items-center justify-center before:absolute before:inset-0 before:rounded-full before:bg-primary before:transition-transform before:duration-300 hover:before:scale-105 active:duration-75 active:before:scale-95 sm:px-4 lg:before:border lg:before:border-gray-200 lg:before:bg-gray-100" href="/pages/contact">
                        <span class="relative text-sm font-semibold text-white dark:text-gray-900 lg:text-primary lg:dark:text-white">Get started</span>
                    </a> -->
                        <NuxtLink
                            class="relative flex h-9 w-full items-center justify-center before:absolute before:inset-0 before:rounded-full before:bg-primary before:transition-transform before:duration-300 hover:before:scale-105 active:duration-75 active:before:scale-95 sm:px-4 lg:before:border lg:before:border-gray-200 lg:before:bg-gray-100"
                            to="/jobs/post">
                            <span
                                class="relative text-sm font-semibold text-white dark:text-gray-900 lg:text-primary lg:dark:text-white">Post
                                jobs</span>
                        </NuxtLink>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>
