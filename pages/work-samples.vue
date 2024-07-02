<script setup>
const samples = ref([])
$fetch('/data/work-samples.json').then(res => {
    samples.value = res.workSamples;
});


</script>

<template>
<NuxtLayout name="master">
    <div class="px-2 mb-10 mt-10">
                <section class="grid mt-6 grid-cols-2 max-sm:grid-cols-1 gap-6 ltr:text-left ">
                    <article v-for="(sample , index) in samples" :key="index">
                        <figure class="h-52 relative group overflow-hidden border-[1px] rounded-xl">
                            <NuxtLink to="/samples" class="flex rtl:flex-row-reverse ltr:flex-row-reverse items-center justify-center text-light font-semibold absolute opacity-0 visibility-hidden transition-all duration-500 hover:opacity-100 group-hover:visibility-visible top-0 right-0 w-full h-full bg-primary-active/80">
                                <span>View the Zoom information</span>
                                <i class="fi fi-br-arrow-right flex ml-2 mt-1"></i>
                            </NuxtLink>
                            <img v-if="!sample.image" class="w-full object-cover h-full" src="/images/image-not-found.webp" :alt="sample.title">
                            <img v-else class="w-full object-cover h-full" :src="sample.image" :alt="sample.title">
                        </figure>
                        <div class="p-2">
                            <h3 class="font-semibold">{{ sample.title }}</h3>
                            <p class="text-xs">{{ sample.description }}</p>
                        </div>
                    </article>
                </section>
            </div>
</NuxtLayout>
</template>