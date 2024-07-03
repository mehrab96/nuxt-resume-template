<script setup>
const bio = ref('');
const fieldActivity = ref([]);
const skills = ref([]);
$fetch('/data/about-me.json').then(res => {
    bio.value = res.bio;
    fieldActivity.value = res.fieldActivity;
    skills.value = res.skills;
});


useHead({
  title: 'Mehrab Esmailnia Personal Resume',
  meta: [
    { name: 'description', content: 'I am a senior software engineer specializing in Laravel and Nuxt.js. Over the past five years, I have developed robust backend applications using Laravel and high-performance, server-side rendered frontend applications with Nuxt.js. Additionally, I have extensive experience building intuitive admin panels with Laravel and Vue.js, enhancing the management of complex systems' }
]});


</script>

<template>

<NuxtLayout name="master">
    <div class="px-2 mb-10 mt-10">
        <div class="highlight">
                <span class="font-black text-xl text-primary-active relative">About me</span>
                <p class="font-extralight ltr:font-light text-base text-primary-active text-justify leading-9 opacity-90">{{ bio }}</p>
        </div>
        <div class="py-6">
            <div class="highlight">
                <span class="font-black text-primary-active text-xl relative">Field of activity</span>
            </div>
            <section class="grid grid-cols-2 max-sm:grid-cols-1 gap-4 mt-4">
                <article v-for="(field , index) in fieldActivity" :key="index" class="h-52 grid justify-center content-center bg-light-white shadow-[0_0_20px] shadow-gray-600/10 rounded-3xl">
                    <figure class="grid justify-center h-16"><img class="w-full h-16 object-contain" :src="field.image" :alt="field.title"></figure>
                    <h2 class="text-center font-black mt-3 pb-1 text-xl text-primary-active">{{field.title}}</h2>
                    <p class="text-center px-12 font-light text-sm text-primary-active/70">{{ field.explanation }}</p>
                </article>
            </section>
        </div>
        <div class="py-6">
            <div class="highlight">
                <span class="font-black text-black/80 text-xl relative">My skills</span>
            </div>
            <section class="grid grid-cols-1 gap-4 mt-4">
                <article v-for="(skill , index) in skills" :key="index" class="w-full h-10 bg-gray-200 rounded-full">
                    <div class="relative overflow-hidden transition-all duration-[3000ms] h-full leading-[2.5rem] bg-blue-600 text-xs font-medium text-blue-100 text-center p-0.5 rounded-full" :style="{width: skill.percent + '%'}">
                        <span class="absolute left-6 top-0 z-30 text-sm leading-[2.4rem] font-semibold">{{skill.title}}</span>
                        <span class="absolute right-6 top-0 font-semibold z-30">%{{skill.percent}}</span>
                    </div>
                </article>
            </section>
        </div>
    </div>

</NuxtLayout>

</template>