<template>
  <div class="nc-HeaderLogged sticky top-0 w-full z-40">
    <div
      class="nc-MainNav2Logged relative z-10 bg-white dark:bg-neutral-900 border-b border-slate-100 dark:border-slate-700">
      <div class="container">
        <div class="h-20 flex justify-between">
          <slot />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "TopbarWrapperComponent"
}
</script>
