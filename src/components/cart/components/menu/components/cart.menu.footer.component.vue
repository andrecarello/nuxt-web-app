<template>
    <div class="bg-neutral-50 dark:bg-slate-900 p-5">
        <p class="flex justify-between font-semibold text-slate-900 dark:text-slate-100">
            <span>
                <span>Subtotal</span>
                <span class="block text-sm text-slate-500 dark:text-slate-400 font-normal">
                    Shipping and taxes calculated at checkout.
                </span>
            </span>
            <span>$299.00</span>
        </p>
        <div class="flex space-x-2 mt-5">
            <button-component variant="secondary" to="/cart">View Cart</button-component>
            <button-component variant="primary" href="/checkout">Check Out</button-component>
        </div>
    </div>
</template>
<script>
import ButtonComponent from '~/components/button/button.component.vue'

export default {
    name: "CartMenuFooterComponent",
    components: { ButtonComponent }
}
</script>