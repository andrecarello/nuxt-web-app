<template>
    <Popover v-slot="{ open }" class="relative">
        <PopoverButton :class="open ? '' : 'text-opacity-90'"
            class="w-10 h-10 sm:w-12 sm:h-12 rounded-full text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 focus:outline-none flex items-center justify-center">
            <!-- <slot name="icon" /> -->
            <component :is="icon" />

            <div v-if="quantity"
                class="w-3.5 h-3.5 flex items-center justify-center bg-primary-500 absolute top-1.5 right-1.5 rounded-full text-[10px] leading-none text-white font-medium">
                <span class="mt-[1px]">3</span>
            </div>
        </PopoverButton>

        <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1"
            enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150"
            leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
            <PopoverPanel class="absolute z-10 w-screen max-w-[260px] px-4 mt-3.5 -right-10 sm:right-0 sm:px-0">
                <slot name="content" />
            </PopoverPanel>
        </transition>
    </Popover>
</template>
<script>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'

export default {
    name: "TopbarDropdownComponent",
    props: {
        icon: 'iconUser',
        quantity: {
            type: Number,
            required: false,
            default: null
        }
    },
    components: {
        Popover,
        PopoverButton,
        PopoverPanel
    }
}
</script>