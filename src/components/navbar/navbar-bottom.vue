<template>

    <nav class="bg-white h-28 shadow-lg">
        <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
            <div class="relative flex h-16 items-center justify-between">
                <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">

                    <button type="button"
                        class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
                        aria-controls="mobile-menu" aria-expanded="false">
                        <span class="absolute -inset-0.5"></span>
                        <span class="sr-only">Open main menu</span>

                        <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                        </svg>

                        <svg class="hidden h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                        </svg>
                    </button>
                </div>
                <div class="flex flex-1 mt-10 items-center justify-center sm:items-stretch sm:justify-start">
                    <div class="flex flex-shrink-0 items-center">
                        <img class="h-10 w-auto"
                            src="https://raw.githubusercontent.com/0rangebananaspy/cdn/main/uploads/fkmunej-agrocoastal-2023.png"
                            alt="Your Company">
                    </div>
                    <div class="hidden sm:mx-auto sm:block ">
                        <div class="flex  space-x-4">
                            <NavbarButton text="Home" :active="{active:activeItem === 1}" @click="toggleActive(1)"></NavbarButton>
                            <NavbarButton text="Staff"></NavbarButton>
                            <NavbarButton text="Journal"></NavbarButton>
                            <NavbarButton text="News" ></NavbarButton>
                        </div>
                    </div>
                </div>
                <div
                    class="absolute inset-y-0 mt-10 right-0 flex items-center pr-3 sm:static sm:inset-auto sm:ml-6 sm:pr-0">
                    <shadow-button text="Website FKM" url="https://fkm.unej.ac.id" target="_blank" color="purple" class="ml-3 pt-3 pb-3 pr-4 pl-6" iconClass="fa-duotone fa-1x animate-spin fa-globe mr-3 mt-1"></shadow-button>
                </div>
            </div>
        </div>


        <div class="sm:hidden" id="mobile-menu">
            <div class="space-y-1 px-2 pb-3 pt-2">

                <a href="#" class="bg-gray-900 text-white block rounded-md px-3 py-2 text-base font-medium"
                    aria-current="page">Dashboard</a>
                <a href="#"
                    class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium">Team</a>
                <a href="#"
                    class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium">Projects</a>
                <a href="#"
                    class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium">Calendar</a>
            </div>
        </div>
    </nav>

</template>
<script setup>

import NavbarButton from '@/elements/NavbarButton.vue';
import ShadowButton from '@/elements/ShadowButton.vue';

import {ref} from 'vue'

const activeItem = ref(1)

const toggleActive = (index) => {
    activeItem.value = activeItem.value === index ? null : index
}

</script>