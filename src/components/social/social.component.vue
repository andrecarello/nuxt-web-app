<template>
    <div class="nc-SocialsList flex space-x-2.5 text-2xl text-neutral-6000 dark:text-neutral-300 mr-auto">
        <a v-for="{ image, text }, index in data" :key="index" href="#"
            class="w-7 h-7 sm:w-8 sm:h-8 flex items-center justify-center rounded-full text-xl">
            <img :src="image.src" :alt="image.alt ? image.alt : text" style="color: transparent" />
        </a>
    </div>
</template>
<script setup>
defineProps({
    data: []
})
</script>
