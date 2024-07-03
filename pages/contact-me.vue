<script setup>

useHead({
  title: 'Mehrab Esmailnia - contact',
  meta: [
    { name: 'description', content: 'I am a senior software engineer specializing in Laravel and Nuxt.js. Over the past five years, I have developed robust backend applications using Laravel and high-performance, server-side rendered frontend applications with Nuxt.js. Additionally, I have extensive experience building intuitive admin panels with Laravel and Vue.js, enhancing the management of complex systems' }
]});

</script>

<template>
<NuxtLayout name="master">
    <div class="px-2 mb-10 mt-10">
        <div class="highlight">
            <span class="font-black text-xl text-primary-active relative">Contact me</span>
        </div>
        <form class="grid grid-cols-2 gap-4 mt-8">
            <div class="grid grid-cols-1 max-sm:col-span-2 relative">
                <label class="font-light text-primary-active/90 text-sm px-2">
                    <span>Fullname</span>
                </label>
                <input class="focus:outline-0 placeholder-font-extralight focus:ring-0
                focus:border-gray-300/20 p-4 mt-2 h-14 rounded-xl text-sm border-gray-300/20 bg-gray-200/20"
                type="text" placeholder="Please enter your fullname">
            </div>
            <div class="grid grid-cols-1 max-sm:col-span-2 relative">
                <label class="font-light text-primary-active/90 text-sm px-2">
                    <span>Email</span>
                </label>
                <input class="focus:outline-0 placeholder-font-extralight focus:ring-0
                focus:border-gray-300/20 p-4 mt-2 h-14 rounded-xl text-sm border-gray-300/20 bg-gray-200/20" type="email" placeholder="Please enter your email">
            </div>
            <div class="grid grid-cols-1 relative col-span-2">
                <label class="font-light text-primary-active/90 text-sm px-2">
                    <span>Message</span>
                </label>
                <textarea class="focus:outline-0 placeholder-font-extralight focus:ring-0 focus:border-gray-300/20
                p-4 mt-2 rounded-xl text-sm border-gray-300/20 bg-gray-200/20 h-96 resize-none" placeholder="Please enter your message"></textarea>
            </div>
            <div class="grid col-span-2 justify-center mt-4">
                <button class="bg-primary-active/10 rounded-full px-12 py-2 text-primary-active font-semibold">
                    <span class="w-full h-full font-semibold">Send Message</span>
                </button>
            </div>
        </form>
    </div>
</NuxtLayout>
</template>