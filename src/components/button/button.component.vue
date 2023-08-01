<template>
    <component :is="component" :to="to" :href="href"
        :class="['nc-Button relative h-auto inline-flex items-center justify-center rounded-full transition-colors text-sm sm:text-base font-medium py-3 px-4 sm:py-3.5 sm:px-6', theme]">
        <slot />
    </component>
</template>
<script setup>
const props = defineProps({
    to: String,
    href: String,
    variant: {
        default: 'primary'
    }
})
console.log(props)
const component = computed(() => {
    if (props.to) return defineNuxtLink({})
    else if (props.href) return 'a'
    else return 'button'
})
console.log(component)
const theme = computed(() => {
    if (props.variant === "secondary") {
        return 'ttnc-ButtonSecondary bg-white text-slate-700 dark:bg-slate-900 dark:text-slate-300 hover:bg-gray-100 dark:hover:bg-slate-800 flex-1 border border-slate-200 dark:border-slate-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-primary-6000 dark:focus:ring-offset-0'
    } else if (props.variant === "primary") {
        return 'ttnc-ButtonPrimary disabled:bg-opacity-90 bg-slate-900 dark:bg-slate-100 hover:bg-slate-800 text-slate-50 dark:text-slate-800 shadow-xl flex-1 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-primary-6000 dark:focus:ring-offset-0'
    }
    return ''
})
</script>


