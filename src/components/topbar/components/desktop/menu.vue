<template>
    <Popover v-for="{ title, links }, index in data" v-slot="{ open }" :key="index"
        class="menu-item menu-dropdown relative">
        <div class="h-20 flex-shrink-0 flex items-center" @mouseover="open = true" @mouseleave="open = false">
            <PopoverButton
                class="inline-flex items-center text-sm lg:text-[15px] font-medium text-slate-700 dark:text-slate-300 py-2.5 px-4 xl:px-5 rounded-full hover:text-slate-900 hover:bg-slate-100 dark:hover:bg-slate-800 dark:hover:text-slate-200">
                {{ title }}
                <chevron-down-icon class="ml-1 -mr-1 h-4 w-4 text-slate-400" />
            </PopoverButton>
        </div>

        <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1"
            enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150"
            leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
            <PopoverPanel class="sub-menu absolute transform z-10 w-56 top-full left-0">
                <ul
                    class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 dark:ring-white dark:ring-opacity-10 text-sm relative bg-white dark:bg-neutral-900 py-4 grid space-y-1">
                    <li v-for="{ title, href }, index in links" :key="index" class="px-2">
                        <a class="flex items-center font-normal text-neutral-6000 dark:text-neutral-400 py-2 px-4 rounded-md hover:text-neutral-700 hover:bg-neutral-100 dark:hover:bg-neutral-800 dark:hover:text-neutral-200"
                            :href="href">{{ title }}
                        </a>
                    </li>
                </ul>
            </PopoverPanel>
        </transition>
    </Popover>
</template>
<script setup>
const open = ref(false)

const props = defineProps({
    data: []
})

console.log(props.data)
import { Popover, PopoverButton, PopoverPanel } from "@headlessui/vue"
import { ChevronDownIcon } from "@heroicons/vue/24/outline"
</script>