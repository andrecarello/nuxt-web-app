<template>
  <topbar-wrapper-component>
    <div class="flex items-center lg:hidden flex-1">
      <button
        class="p-2.5 rounded-lg text-neutral-700 dark:text-neutral-300 focus:outline-none flex items-center justify-center">
        <IconsRender icon="iconHamburguer" class="h-7 w-7" />
        <!-- <icon-hamburguer class="h-7 w-7" /> -->
      </button>
    </div>

    <div class="lg:flex-1 flex items-center">
      <topbar-brand-component />
    </div>

    <div class="flex-[2] hidden lg:flex justify-center mx-4">
      <div class="nc-Navigation flex items-center">
        <menu-desktop :data="[
          { title: 'Verão', links: [{ title: 'Verão Frio', href: '/collection' }, { title: 'Verão Claro', href: '/collection' }] },
          { title: 'Inverno', links: [{ title: 'Inverno Escuro', href: '/collection' }, { title: 'Inverno Frio', href: '/collection' }] },
          { title: 'Primavera', links: [{ title: 'Primavera Brilhante', href: '/collection' }, { title: 'Primavera Clara', href: '/collection' }, { title: 'Primavera Quente', href: '/collection' }] },
          { title: 'Outono', links: [{ title: 'Outono Escuro', href: '/collection' }, { title: 'Outono Quente', href: '/collection' }, { title: 'Outono Suave', href: '/collection' }] },
        ]"></menu-desktop>

        <menu-mobile :is-open="false" :data="[
          { title: 'Verão', links: [{ title: 'Verão Frio', href: '/collection' }, { title: 'Verão Claro', href: '/collection' }] },
          { title: 'Inverno', links: [{ title: 'Inverno Escuro', href: '/collection' }, { title: 'Inverno Frio', href: '/collection' }] },
          { title: 'Primavera', links: [{ title: 'Primavera Brilhante', href: '/collection' }, { title: 'Primavera Clara', href: '/collection' }, { title: 'Primavera Quente', href: '/collection' }] },
          { title: 'Outono', links: [{ title: 'Outono Escuro', href: '/collection' }, { title: 'Outono Quente', href: '/collection' }, { title: 'Outono Suave', href: '/collection' }] },
        ]"></menu-mobile>
      </div>
    </div>

    <div class="flex-1 flex items-center justify-end text-slate-700 dark:text-slate-100">
      <topbar-button-component class="hidden lg:flex">
        <iconSearch class="w-6 h-6" />
      </topbar-button-component>

      <topbar-dropdown-component :icon="iconUser">
        <!-- <template #icon>
          <iconUser class="w-6 h-6" />
        </template> -->
        <template #content>
          <div class="overflow-hidden rounded-3xl shadow-lg ring-1 ring-black ring-opacity-5">
            <div class="relative grid grid-cols-1 gap-6 bg-white dark:bg-neutral-800 py-7 px-6">
              <div class="flex items-center space-x-3">
                <div
                  class="wil-avatar relative flex-shrink-0 inline-flex items-center justify-center text-neutral-100 uppercase font-semibold shadow-inner rounded-full w-12 h-12 ring-1 ring-white dark:ring-neutral-900">
                  <img
                    src="https://as2.ftcdn.net/v2/jpg/02/31/85/47/1000_F_231854793_01AdcYiVmFpVpzJfM0d3ghLvT6tZ3T4t.jpg"
                    class="absolute inset-0 w-full h-full object-cover rounded-full" />
                </div>
                <div class="flex-grow">
                  <h4 class="font-semibold">Eden Smith</h4>
                  <p class="text-xs mt-0.5">Los Angeles, CA</p>
                </div>
              </div>

              <div class="w-full border-b border-neutral-200 dark:border-neutral-700" />

              <topbar-dropdown-link-component label="My Account">
                <user-icon class="w-6 h-6" />
              </topbar-dropdown-link-component>
              <topbar-dropdown-link-component label="My Order">
                <icon-order class="w-6 h-6" />
              </topbar-dropdown-link-component>
              <topbar-dropdown-link-component label="Wishlist">
                <heart-icon class="w-6 h-6" />
              </topbar-dropdown-link-component>

              <div class="w-full border-b border-neutral-200 dark:border-neutral-700" />

              <topbar-dropdown-link-component :special="true" label="Dark Theme">
                <light-bulb-icon class="w-6 h-6" />
                <template #special>
                  <Switch v-model="enabled"
                    :class="[enabled ? 'bg-teal-900' : 'bg-teal-600', 'relative inline-flex h-[22px] w-[42px] shrink-0 cursor-pointer rounded-full border-4 border-transparent transition-colors duration-200 ease-in-out focus:outline-none focus-visible:ring-2  focus-visible:ring-white focus-visible:ring-opacity-75']">
                    <span class="sr-only">Use setting</span>
                    <span aria-hidden="true" :class="enabled ? 'translate-x-5' : 'translate-x-0'"
                      class="pointer-events-none inline-block h-[14px] w-[14px] transform rounded-full bg-white shadow-lg ring-0 transition duration-200 ease-in-out" />
                  </Switch>
                </template>
              </topbar-dropdown-link-component>
              <topbar-dropdown-link-component label="Help">
                <lifebuoy-icon class="w-6 h-6" />
              </topbar-dropdown-link-component>
              <topbar-dropdown-link-component label="Log Out">
                <arrow-left-on-rectangle-icon class="w-6 h-6" />
              </topbar-dropdown-link-component>
            </div>
          </div>
        </template>
      </topbar-dropdown-component>


      <topbar-dropdown-component :quantity="3">
        <template #icon>
          <icon-shopping-cart class="w-6 h-6" />
        </template>
        <template #content>
          <cart-menu-component />
        </template>
      </topbar-dropdown-component>
    </div>
  </topbar-wrapper-component>
</template>

<script setup>
import { ref } from "vue"

import { Switch } from "@headlessui/vue"
import iconHamburguer from "../icons/icon.hamburguer.vue";
import iconUser from "../icons/icon.user.vue";
import iconSearch from "../icons/icon.search.vue";
import iconShoppingCart from "../icons/icon.shopping.cart.vue";
import iconOrder from "../icons/icon.order.vue"
import { UserIcon, HeartIcon, LightBulbIcon, LifebuoyIcon, ArrowLeftOnRectangleIcon } from "@heroicons/vue/24/outline"
import TopbarBrandComponent from "./components/topbar.brand.component.vue";
import TopbarWrapperComponent from "./components/topbar.wrapper.component.vue";
import TopbarButtonComponent from "./components/topbar.button.component.vue";
import TopbarDropdownComponent from "./components/topbar.dropdown.component.vue"
import TopbarDropdownLinkComponent from './components/topbar.dropdown.item.component.vue';
import CartMenuComponent from "../cart/components/menu/cart.menu.component.vue";
import MenuDesktop from "./components/desktop/menu.vue";
import MenuMobile from "./components/mobile/menu.vue";

const enabled = ref(false)
</script>