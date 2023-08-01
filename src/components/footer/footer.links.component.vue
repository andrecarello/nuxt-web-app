<template>
  <h2 class="font-semibold text-neutral-700 dark:text-neutral-200">
    {{ heading }}
  </h2>
  <ul class="mt-5 space-y-4">
    <li v-for="{ href, text, target, index } in data" :key="index">
      <a
        class="text-neutral-6000 dark:text-neutral-300 hover:text-black dark:hover:text-white"
        :href="href"
        :target="target"
        rel="noopener noreferrer"
        >{{ text }}</a
      >
    </li>
  </ul>
</template>
<script lang="ts">
import { defineComponent, PropType } from "vue";

interface FooterLinksInterface {
  heading: string;
  data: {
    href: string;
    target: "_blank" | "_self";
    text: string;
    index?: number
  }[];
}

export default defineComponent({
  name: "FooterLinksComponent",

  props: {
    heading: {
      type: Object as PropType<FooterLinksInterface["heading"]>,
      required: false,
    },
    data: {
      type: Object as PropType<FooterLinksInterface["data"]>,
      required: true,
    },
  },
});
</script>