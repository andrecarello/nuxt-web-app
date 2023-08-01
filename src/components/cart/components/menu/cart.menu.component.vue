<template>
    <div class="hidden md:block absolute z-10 w-screen max-w-xs sm:max-w-md px-4 -right-28 sm:right-0 sm:px-0 opacity-100 translate-y-0"
        tabindex="-1">
        <div class="overflow-hidden rounded-2xl shadow-lg ring-1 ring-black/5 dark:ring-white/10">
            <div class="relative bg-white dark:bg-neutral-800">
                <div class="max-h-[60vh] p-5 overflow-y-auto hiddenScrollbar">
                    <h3 class="text-xl font-semibold">Shopping cart</h3>
                    <div class="divide-y divide-slate-100 dark:divide-slate-700">
                        <cart-menu-item-component />
                        <cart-menu-item-component />
                        <cart-menu-item-component />
                    </div>
                </div>
                <cart-menu-footer-component />
            </div>
        </div>
    </div>
</template>
<script>
import CartMenuFooterComponent from './components/cart.menu.footer.component.vue'
import CartMenuItemComponent from "./components/cart.menu.item.component.vue"

export default {
    name: "CartMenuComponent",
    components: { CartMenuItemComponent, CartMenuFooterComponent }
}
</script>