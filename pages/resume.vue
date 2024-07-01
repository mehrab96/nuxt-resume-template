<script setup>
const experiences = ref([]);
const educations = ref([]);
$fetch('/data/resume.json').then(res => {
    experiences.value = res.experiences;
    educations.value = res.educations;
});


</script>

<template>
<NuxtLayout name="master">
    <div class="px-2 mb-10 mt-10">
        <div class="highlight">
            <span class="font-black text-xl text-primary-active relative">My resume</span>
        </div>
        <div class="mt-8">
            <div class="grid grid-cols-[auto_auto] gap-2 items-center justify-start font-black text-primary-active text-xl">
                <div class="h-9 w-11 grid justify-center items-center border-[.17rem] border-primary-active border-solid rounded-md">
                    <i class="fi fi-rr-brain-circuit text-2xl flex"></i>
                </div>
                <span class="mt-1">My Experiences</span>
            </div>
            <ul class="mt-10 relative pl-10 before:absolute before:bg-primary-medium/40 before:content[''] before:top-1 before:left-3.5 before:h-full before:w-[1.5px]">
                <li v-for="(experience , index) in experiences" class="mb-8 relative circleOverLi" :key="index">
                    <h4 class="font-black text-primary-active text-md">{{ experience.title }}</h4>
                    <span class="font-mono font-black text-sm text-primary-active/90">{{experience.date}}</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">{{ experience.explanation }}</p>
                </li>
            </ul>
        </div>
        <div class="mt-8">
            <div class="grid grid-cols-[auto_auto] gap-2 items-center justify-start font-black text-primary-active text-xl">
                <div class="h-9 w-11 grid justify-center items-center border-[.17rem] border-primary-active border-solid rounded-md">
                    <i class="fi fi-rr-e-learning text-2xl flex"></i>
                </div>
                <span class="mt-1">My Education</span>
            </div>
            <ul class="mt-10 relative pl-10 before:absolute before:bg-primary-medium/40 before:content[''] before:top-1 before:left-3.5 before:h-full before:w-[1.5px]">
                <li v-for="(education , index) in educations" :key="index" class="mb-8 relative circleOverLi">
                    <h4 class="font-semibold ltr:font-black text-primary-active text-md">{{ education.title }}</h4>
                    <span class="ltr:font-mono text-sm font-semibold text-primary-active/90">{{education.date}}</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">{{ education.explanation }}</p>
                </li>
            </ul>
        </div>
    </div>
</NuxtLayout>
</template>