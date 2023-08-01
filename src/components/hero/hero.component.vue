<template>
  <div
    class="nc-SectionHero2Item nc-SectionHero2Item--animation flex flex-col-reverse lg:flex-col relative overflow-hidden">
    <div class="absolute bottom-4 left-1/2 -translate-x-1/2 z-20 flex justify-center">
      <div class="relative px-1 py-1.5 cursor-pointer">
        <div class="relative w-20 h-1 shadow-sm rounded-md bg-white">
          <div class="nc-SectionHero2Item__dot absolute inset-0 bg-slate-900 rounded-md"></div>
        </div>
      </div>
    </div>
    <div
      class="nc-Prev text-slate-500 dark:text-slate-400 absolute left-1 sm:left-5 top-3/4 sm:top-1/2 sm:-translate-y-1/2 z-10 !text-slate-700"
      data-glide-el="controls">
      <button
        class="w-12 h-12 hover:border-slate-400 dark:hover:border-slate-400 rounded-full flex items-center justify-center border-2 hover:border-slate-200 dark:hover:border-slate-600 border-transparent"
        title="Prev" data-glide-dir="<">
        <ArrowLeftIcon class="w-6 h-6" />
      </button>
    </div>
    <div
      class="nc-Next text-slate-500 dark:text-slate-400 absolute right-1 sm:right-5 top-3/4 sm:top-1/2 sm:-translate-y-1/2 z-10 !text-slate-700"
      data-glide-el="controls">
      <button
        class="w-12 h-12 hover:border-slate-400 dark:hover:border-slate-400 rounded-full flex items-center justify-center border-2 hover:border-slate-200 dark:hover:border-slate-600 border-transparent"
        title="Next" data-glide-dir=">">
        <ArrowRightIcon class="w-6 h-6" />
      </button>
    </div>
    <div class="absolute inset-0 bg-[#E3FFE6]">
      <img alt="hero" loading="lazy" decoding="async" data-nimg="fill" class="absolute w-full h-full object-contain"
        style="
          position: absolute;
          height: 100%;
          width: 100%;
          left: 0;
          top: 0;
          right: 0;
          bottom: 0;
          color: transparent;
        " src="~/assets/img/Moon.9de4dde7.svg" />
    </div>
    <div class="relative container pb-0 pt-14 sm:pt-20 lg:py-44">
      <div class="relative z-[1] w-full max-w-3xl space-y-8 sm:space-y-14 nc-SectionHero2Item__left">
        <div class="space-y-5 sm:space-y-6">
          <span class="nc-SectionHero2Item__subheading block text-base md:text-xl text-slate-700 font-medium">Aproveite o
            verão 🔥</span>
          <h2
            class="nc-SectionHero2Item__heading font-semibold text-3xl sm:text-4xl md:text-5xl xl:text-6xl 2xl:text-7xl !leading-[114%] text-slate-900">
            Coleção exclusiva para combinar com você!
          </h2>
        </div>

        <button-component class="py-3 px-6 sm:py-5 sm:px-9 nc-SectionHero2Item__button" to="/">
          <span>Quero aproveitar!</span>
          <iconSearch class="w-5 h-5 ml-2.5" />
        </button-component>
      </div>
      <div class="mt-10 lg:mt-0 lg:absolute right-0 bottom-0 top-0 w-full max-w-2xl xl:max-w-3xl 2xl:max-w-4xl">
        <img src="~/assets/img/hero-right-2.webp" alt="Coleção exclusiva para combinar com você!"
          class="w-full h-full object-contain object-right-bottom nc-SectionHero2Item__image" style="
            position: absolute;
            height: 100%;
            width: 100%;
            left: 0;
            top: 0;
            right: 0;
            bottom: 0;
            color: transparent;
          " />
      </div>
    </div>
  </div>
</template>

<script setup>
import iconSearch from "../icons/icon.search.vue"
import { ArrowLeftIcon, ArrowRightIcon } from "@heroicons/vue/24/outline";
import ButtonComponent from "../button/button.component.vue"
</script>