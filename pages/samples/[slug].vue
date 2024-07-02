<script setup>
const sample = ref({});
const route = useRoute();

$fetch('/data/work-samples.json').then(res => {
    sample.value = res.workSamples.filter(item => {
        return item.slug == route.params.slug
    })[0];
});


</script>

<template>
<NuxtLayout name="master">
    <div class="px-2 mb-10 mt-10">
                <NuxtLink to="/work-samples" class="mb-12 grid grid-cols-[auto,auto] justify-start gap-2 items-center">
                    <i class="fi fi-rr-arrow-left text-primary-active flex"></i>
                    <span class="font-bold text-sm text-primary-active">Back to samples</span>
                </NuxtLink>
                <section class="grid mt-6 grid-cols-1 gap-6">
                    <figure class="rounded-xl border-[1px] w-full h-auto -mt-8 overflow-hidden max-h-[30rem]">
                        <img v-if="!sample.image" class="w-full object-cover h-full" src="/images/image-not-found.webp" :alt="sample.title">
                        <img v-else class="w-full object-cover h-full" :src="sample.image" :alt="sample.title">
                    </figure>
                    <div class="grid grid-cols-[auto,auto] -mt-12 gap-4 justify-center">
                        <NuxtLink target="_blank" class="bg-white px-8 pr-10 flex items-center gap-2 text-sm font-semibold h-10 shadow-xl rounded-3xl text-primary-active" :href="`https://${sample.previewLink}`" :title="sample.title" :name="sample.title">
                            <i class="fi fi-rr-link-alt text-base flex"></i>
                            <span>{{ sample.previewLink }}</span>
                        </NuxtLink>
                    </div>
                    <h1 class="font-extrabold text-2xl mt-2">{{ sample.title }}</h1>
                    <p class="leading-8 bg-primary/10 rounded-xl mb-0 p-4 text-primary-active font-extralight">
                       {{ sample.description }}
                    </p>
                    <div class="bodyStyle" v-html="sample.body">
                        
                    </div>
                </section>
            </div>
</NuxtLayout>
</template>