<template>
  <a
    href="#"
    class="flex items-center text-2xl text-neutral-700 hover:text-black dark:text-neutral-300 dark:hover:text-white leading-none space-x-2 group"
  >
    <div class="flex-shrink-0 w-5">
      <img
        :src="image.src"
        :alt="image.alt"
        loading="lazy"
        width="136"
        height="136"
        decoding="async"
        style="color: transparent"
      />
    </div>
    <span class="hidden lg:block text-sm">{{ text }}</span>
  </a>
</template>
<script lang="ts">
import { defineComponent, PropType } from "vue";

interface FooterSocialInterface {
  text: string;
  image: {
    src: string;
    alt: string;
  }[];
}

export default defineComponent({
  name: "FooterLinksComponent",

  props: {
    text: {
      type: Object as PropType<FooterSocialInterface["text"]>,
      required: false,
    },
    image: {
      type: Object as PropType<FooterSocialInterface["image"]>,
      required: true,
    },
  },
});
</script>
