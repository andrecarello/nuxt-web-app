<template>
    <TransitionRoot appear :show="isOpen" as="template">
        <Dialog as="div" @close="onClose" class="fixed inset-0 z-50 overflow-y-auto">

            <div class="fixed left-0 top-0 bottom-0 w-full max-w-md md:w-auto z-max outline-none focus:outline-none">
                <TransitionChild as="template" enter="transition duration-100 transform"
                    enter-from="opacity-0 -translate-x-14" enter-to="opacity-100 translate-x-0"
                    leave="transition duration-150 transform" leave-from="opacity-100 translate-x-0"
                    leave-to="opacity-0 -translate-x-14">
                    <div class="z-20 relative">
                        <div
                            class="overflow-y-auto w-full h-screen py-2 transition transform shadow-lg ring-1 dark:ring-neutral-700 bg-white dark:bg-neutral-900 divide-y-2 divide-neutral-100 dark:divide-neutral-800">

                            <div class="py-6 px-5">

                                <NuxtLink to="/">
                                    <img src="~/assets/img/comcor-logo.webp" alt="ComCor"
                                        class="block h-32 sm:h-24 w-auto mt-10" />
                                </NuxtLink>

                                <div class="flex flex-col mt-5 text-slate-600 dark:text-slate-300 text-sm">
                                    <span>
                                        Discover the most outstanding articles on all topics of life. Write
                                        your stories and share them
                                    </span>

                                    <div class="flex justify-between items-center mt-4">
                                        <social-component :data="[
                                            {
                                                text: 'Facebook',
                                                image: { src: '/assets/img/facebook.f8b5f526.svg' },
                                                to: 'https://facebook.com'
                                            },
                                            {
                                                text: 'Twitter',
                                                image: { src: '/assets/img/twitter.5b2905e9.svg' },
                                                to: 'https://twitter.com'
                                            },
                                            {
                                                text: 'Youtube',
                                                image: { src: '/assets/img/youtube.fb347fb8.svg' },
                                                to: 'https://music.youtube.com/watch?v=NxxjLD2pmlk&list=RDAMVMmQryrzpr0H0'
                                            },
                                            {
                                                text: 'Telegram',
                                                image: { src: '/assets/img/telegram.513d1435.svg' },
                                                to: 'https://web.telegram.org/'
                                            }
                                        ]" />
                                    </div>

                                    <div class="mt-5">
                                        <form action="" method="POST" class="flex-1 text-slate-900 dark:text-slate-200">
                                            <div
                                                class="bg-slate-50 dark:bg-slate-800 flex items-center space-x-1 py-2 px-4 rounded-xl h-full">
                                                <icon-search class="w-6 h-6" />
                                                <input type="search" placeholder="Type and press enter"
                                                    class="border-none bg-transparent focus:outline-none focus:ring-0 w-full text-sm " />
                                            </div>
                                        </form>
                                    </div>
                                </div>
                            </div>

                            <ul class="flex flex-col py-6 px-2 space-y-1">
                                <Disclosure v-for="{ title, links }, index in data" :key="index" as="li"
                                    class="text-slate-900 dark:text-white">
                                    <DisclosureButton
                                        class="flex w-full items-center py-2.5 px-4 font-medium uppercase tracking-wide text-sm hover:bg-slate-100 dark:hover:bg-slate-800 rounded-lg">
                                        <span class="mr-auto">{{ title }}</span>
                                        <ChevronDownIcon class="ml-2 h-4 w-4 text-neutral-500" />
                                    </DisclosureButton>
                                    <DisclosurePanel class="text-gray-500">
                                        <ul class="nav-mobile-sub-menu pl-6 pb-1 text-base">
                                            <DisclosureButton v-for="{ title, href }, index in links" :key="index" as="li">
                                                <NuxtLink :to="href"
                                                    class="flex text-sm rounded-lg hover:bg-neutral-100 dark:hover:bg-neutral-800 mt-0.5 pr-4  pl-3 text-neutral-900 dark:text-neutral-200 font-medium">
                                                    <span class="py-2.5 block w-full">{{ title }}</span>
                                                </NuxtLink>
                                            </DisclosureButton>
                                        </ul>
                                    </DisclosurePanel>
                                </Disclosure>
                            </ul>

                            <div className="absolute right-2 top-2 p-1 border-none">
                                <div
                                    class="cursor-pointer w-8 h-8 flex items-center justify-center rounded-full text-neutral-700 dark:text-neutral-300 hover:bg-neutral-100 dark:hover:bg-neutral-700">
                                    <span className="sr-only">Close</span>
                                    <XMarkIcon class="w-5 h-5" />
                                </div>
                            </div>

                            <div class="flex items-center justify-between py-6 px-5 space-x-2">
                                <button-component variant="primary" href="https://google.com">
                                    Buy this template
                                </button-component>
                            </div>
                        </div>
                    </div>
                </TransitionChild>

                <TransitionChild as="template" enter="duration-300" enter-from="opacity-0" enter-to="opacity-100"
                    leave="duration-200" leave-from="opacity-100" leave-to="opacity-0">
                    <DialogOverlay class="fixed inset-0 bg-neutral-900/60" />
                </TransitionChild>
            </div>

            <TransitionChild as="template" enter="duration-300 ease-out" enter-from="opacity-0" enter-to="opacity-100"
                leave="duration-200 ease-in" leave-from="opacity-100" leave-to="opacity-0">
                <div class="fixed inset-0 bg-black bg-opacity-25" />
            </TransitionChild>
        </Dialog>
    </TransitionRoot>
</template>
<script setup>
import { ref } from "vue"
import {
    TransitionRoot,
    TransitionChild,
    Disclosure,
    DisclosureButton,
    DisclosurePanel,
    Dialog,
    DialogPanel,
    DialogOverlay,
} from "@headlessui/vue"
import SocialComponent from "~/components/social/social.component.vue"
import IconSearch from "../../../icons/icon.search.vue"
import ButtonComponent from "~/components/button/button.component.vue"
import { ChevronDownIcon, XMarkIcon } from "@heroicons/vue/24/outline"

defineEmits(['onClose'])

const props = defineProps({
    isOpen: false,
    data: []
})
</script>