<template>
    <div class="flex py-5 last:pb-0">
        <div class="relative h-24 w-20 flex-shrink-0 overflow-hidden rounded-xl bg-slate-100">
            <a href="">
                <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1399&q=80"
                    alt="" class="h-full w-full object-cover object-center"
                    style="position: absolute; height: 100%; width: 100%; inset: 0px;" />
            </a>
        </div>
        <div class="ml-4 flex flex-1 flex-col">
            <div>
                <div class="flex justify-between">
                    <div>
                        <h3 class="text-base font-medium">
                            <a href="/product-detail">Leather Gloves</a>
                        </h3>
                        <p class="mt-1 text-sm text-slate-500 dark:text-slate-400">
                            <span>Natural</span>
                            <span class="mx-2 border-l border-slate-200 dark:border-slate-700 h-4"></span>
                            <span>XL</span>
                        </p>
                    </div>
                    <div class="mt-0.5">
                        <div
                            class="flex items-center border-2 border-green-500 rounded-lg py-1 px-2 md:py-1.5 md:px-2.5 text-sm font-medium">
                            <span class="text-green-500 !leading-none">$42</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="flex flex-1 items-end justify-between text-sm">
                <p class="text-gray-500 dark:text-slate-400">Qty 1</p>
                <div class="flex">
                    <button type="button" class="font-medium text-primary-6000 dark:text-primary-500 ">Remove</button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {}
</script>