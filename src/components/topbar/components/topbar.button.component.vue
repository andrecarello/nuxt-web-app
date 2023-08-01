<template>
    <button
        class="relative w-10 h-10 sm:w-12 sm:h-12 rounded-full text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 focus:outline-none items-center justify-center">
        <slot />

        <div v-if="quantity"
            class="w-3.5 h-3.5 flex items-center justify-center bg-primary-500 absolute top-1.5 right-1.5 rounded-full text-[10px] leading-none text-white font-medium">
            <span class="mt-[1px]">3</span>
        </div>
    </button>
</template>
<script>
export default {
    name: "TopbarButtonComponent",
    props: {
        quantity: {
            type: Number,
            required: false,
            default: null
        }
    }
}
</script>