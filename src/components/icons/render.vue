<script setup lang="ts">
import iconHamburguer from './icon.hamburguer.vue';

interface IconProps {
    icon: String
}

const prop = defineProps<IconProps>()
</script>

<template>
    <component :is="prop.icon" />
</template>