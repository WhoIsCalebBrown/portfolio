<template>
    <div class="bg-dark-secondary">
        <header class="absolute inset-x-0 top-0 z-50">
            <div class="mx-auto max-w-7xl">
                <div class="px-6 pt-6 lg:max-w-2xl lg:pl-8 lg:pr-0">
                    <nav class="flex items-center justify-between lg:justify-start" aria-label="Global">
                        <a href="#" class="-m-1.5 p-1.5 flex items-center">
                            <span class="sr-only">Caleb Brown</span>
                            <img alt="CalebBrown" class="h-8 w-auto" src="Images/Logo.svg" />
                            <div class="pl-2 text-xl font-semibold text-white">
                                Caleb Brown
                            </div>
                        </a>
                        <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700 lg:hidden" @click="mobileMenuOpen = true">
                            <span class="sr-only">Open main menu</span>
                            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
                        </button>
                        <div class="hidden lg:ml-12 lg:flex lg:gap-x-14">
                            <a v-for="item in navigation" :key="item.name" :href="item.href" class="text-sm font-semibold leading-6 text-white">{{ item.name }}</a>
                        </div>
                    </nav>
                </div>
            </div>
            <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
                <div class="fixed inset-0 z-50" />
                <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-dark-secondary px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
                    <div class="flex items-center justify-between">
                        <a href="#" class="-m-1.5 p-1.5 flex items-center">
                            <span class="sr-only">Caleb Brown</span>
                            <img alt="CalebBrown" class="h-8 w-auto" src="Images/Logo.svg" />
                            <div class="pl-2 text-xl font-semibold text-white">
                                Caleb Brown
                            </div>
                        </a>
                        <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
                            <span class="sr-only">Close menu</span>
                            <XMarkIcon class="h-6 w-6" aria-hidden="true" />
                        </button>
                    </div>
                    <div class="mt-6 flow-root">
                        <div class="-my-6 divide-y divide-gray-500/10">
                            <div class="space-y-2 py-6">
                                <a v-for="item in navigation" :key="item.name" :href="item.href" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-white hover:bg-gray-50">{{ item.name }}</a>
                            </div>
                        </div>
                    </div>
                </DialogPanel>
            </Dialog>
        </header>

        <div class="relative">
            <div class="mx-auto max-w-7xl">
                <div class="relative z-10 pt-14 lg:w-full lg:max-w-2xl">
                    <svg class="absolute inset-y-0 right-8 hidden h-full w-80 translate-x-1/2 transform fill-dark-secondary lg:block" viewBox="0 0 100 100" preserveAspectRatio="none" aria-hidden="true">
                        <polygon points="0,0 90,0 50,100 0,100" />
                    </svg>

                    <div class="relative px-6 py-32 sm:py-40 lg:px-8 lg:py-56 lg:pr-0">
                        <div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-xl">
                            <div class="hidden sm:mb-10 sm:flex">
                                <div class="relative rounded-full px-3 py-1 text-sm leading-6 text-white ring-1 ring-gray-900/10 hover:ring-gray-900/20">
                                    If you would like to see some of my videography! <a href="#" class="whitespace-nowrap font-semibold text-accent"><span class="absolute inset-0" aria-hidden="true" />Click Here<span aria-hidden="true">&rarr;</span></a>
                                </div>
                            </div>
                            <h1 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">I Build & Design <br />
                                Web Interfaces.</h1>
                            <p class="mt-6 text-lg leading-8 text-white">
                                Passionate about fitness, finance, software development,
                                and mountain hiking.
                            </p>
                            <div class="mt-10 flex items-center gap-x-6">
                                <a href="#" class="rounded-md bg-accent px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-accent-hover focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">My Work</a>
                                <a href="#" class="text-sm font-semibold leading-6 text-accent">About Me<span aria-hidden="true">→</span></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="bg-gray-50 lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
                <img class="aspect-[3/2] object-cover lg:aspect-auto lg:h-full lg:w-full" src="Images/Me.jpg" alt="" />
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
    { name: 'Home', href: '#' },
    { name: 'Projects', href: '#' },
    { name: 'Skills', href: '#' },
    { name: 'About', href: '#' },
]

const mobileMenuOpen = ref(false)
</script>
