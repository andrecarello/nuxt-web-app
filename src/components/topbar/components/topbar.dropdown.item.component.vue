<template>
    <component :is="special ? 'div' : 'a'"
        class="flex items-center p-2 -m-3 transition duration-150 ease-in-out rounded-lg hover:bg-neutral-100 dark:hover:bg-neutral-700 focus:outline-none focus-visible:ring focus-visible:ring-orange-500 focus-visible:ring-opacity-50"
        href="/account">
        <div class="flex items-center justify-center flex-shrink-0 text-neutral-500 dark:text-neutral-300">
            <slot />
        </div>
        <p class="ml-4 text-sm font-medium">{{ label }}</p>
        <div v-if="$slots.special" class="ml-auto">
            <slot name="special" />
        </div>
    </component>
</template>
<script>
export default {
    name: "TopbarDropdownItemComponent",
    props: {
        label: String,
        special: Boolean
    }
}
</script>