<script setup>
const samples = ref([])
$fetch('/data/work-samples.json').then(res => {
    samples.value = res.workSamples;
});

useHead({
  title: 'Mehrab Esmailnia work samples',
  meta: [
    { name: 'description', content: 'I am a senior software engineer specializing in Laravel and Nuxt.js. Over the past five years, I have developed robust backend applications using Laravel and high-performance, server-side rendered frontend applications with Nuxt.js. Additionally, I have extensive experience building intuitive admin panels with Laravel and Vue.js, enhancing the management of complex systems' }
]});
</script>

<template>
<NuxtLayout name="master">
    <div class="px-2 mb-10 mt-10">
        <section class="grid mt-6 grid-cols-2 max-sm:grid-cols-1 gap-6 ltr:text-left">
            <article v-for="(sample , index) in samples" :key="index">
                <figure class="h-52 relative group overflow-hidden border-[1px] rounded-xl">
                    <NuxtLink :to="`/samples/${sample.slug}`" :title="sample.title" :name="sample.title" class="flex rtl:flex-row-reverse ltr:flex-row-reverse items-center justify-center text-light font-semibold absolute opacity-0 visibility-hidden transition-all duration-500 hover:opacity-100 group-hover:visibility-visible top-0 right-0 w-full h-full bg-primary-active/80">
                        <span>View the Zoom information</span>
                        <i class="fi fi-rr-arrow-right flex ml-2 mt-1"></i>
                    </NuxtLink>
                    <img v-if="!sample.image" class="w-full object-cover h-full" src="/images/image-not-found.webp" :alt="sample.title">
                    <img v-else class="w-full object-cover h-full" :src="sample.image" :alt="sample.title">
                </figure>
                <div class="p-2">
                    <NuxtLink :to="`/samples/${sample.slug}`" :title="sample.title" :name="sample.title">
                        <h3 class="font-semibold line-clamp-2">{{ sample.title }}</h3>
                    </NuxtLink>
                </div>
            </article>
        </section>
    </div>
</NuxtLayout>
</template>