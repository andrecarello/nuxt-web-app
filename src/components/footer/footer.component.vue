<template>
  <div
    class="nc-Footer relative py-20 lg:pt-28 lg:pb-24 border-t border-neutral-200 dark:border-neutral-700"
  >
    <div
      class="container grid grid-cols-2 gap-y-10 gap-x-5 sm:gap-x-8 md:grid-cols-4 lg:grid-cols-5 lg:gap-x-10"
    >
      <div
        class="grid grid-cols-4 gap-5 col-span-2 md:col-span-4 lg:md:col-span-1 lg:flex lg:flex-col"
      >
        <div class="col-span-2 md:col-span-1">
          <a
            class="ttnc-logo inline-block text-slate-600 flex-shrink-0"
            href="/"
          >
            <img
              src="~/assets/img/comcor-logo.webp"
              alt="ComCor"
              class="block h-32 sm:h-24 w-auto mt-10 dark:hidden"
              style="color: transparent"
            />
            <img
              src="~/assets/img/comcor-logo.webp"
              alt="ComCor"
              class="hidden h-8 sm:h-10 w-auto dark:block"
              style="color: transparent"
            />
          </a>
        </div>
        <div class="col-span-2 flex items-center md:col-span-3">
          <div
            class="nc-SocialsList1 flex items-center space-x-2 lg:space-x-0 lg:flex-col lg:space-y-3 lg:items-start"
            data-nc-id="SocialsList1"
          >
            <footer-social-component
              text="Telegram"
              :image="{ src: '/assets/img/facebook.f8b5f526.svg', alt: '' }"
            />
            <footer-social-component
              text="Telegram"
              :image="{ src: '/assets/img/youtube.fb347fb8.svg', alt: '' }"
            />
            <footer-social-component
              text="Telegram"
              :image="{ src: '/assets/img/telegram.513d1435.svg', alt: '' }"
            />
            <footer-social-component
              text="Twitter"
              :image="{ src: '/assets/img/twitter.5b2905e9.svg', alt: '' }"
            />
          </div>
        </div>
      </div>
      <div class="text-sm">
        <footer-links-component
          heading="Getting started"
          :data="[
            { href: '/', target: '_blank', text: 'Release Notes' },
            { href: '/', target: '_blank', text: 'Upgrade Guide' },
            { href: '/', target: '_blank', text: 'Browser Support' },
            { href: '/', target: '_blank', text: 'Dark Mode' },
          ]"
        />
      </div>
      <div class="text-sm">
        <footer-links-component
          heading="Explore"
          :data="[
            { href: '/', target: '_blank', text: 'Prototyping' },
            { href: '/', target: '_blank', text: 'Design systems' },
            { href: '/', target: '_blank', text: 'Pricing' },
            { href: '/', target: '_blank', text: 'Security' },
          ]"
        />
      </div>
      <div class="text-sm">
        <footer-links-component
          heading="Resources"
          :data="[
            { href: '/', target: '_blank', text: 'Best practices' },
            { href: '/', target: '_blank', text: 'Support' },
            { href: '/', target: '_blank', text: 'Developers' },
            { href: '/', target: '_blank', text: 'Learn design' },
          ]"
        />
      </div>
      <div class="text-sm">
        <footer-links-component
          heading="Community"
          :data="[
            { href: '/', target: '_blank', text: 'Discussion Forums' },
            { href: '/', target: '_blank', text: 'Code of Conduct' },
            { href: '/', target: '_blank', text: 'Contributing' },
            { href: '/', target: '_blank', text: 'API Reference' },
          ]"
        />
      </div>
    </div>
  </div>
</template>