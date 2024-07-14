<script setup>
const personal = ref({});
const socialMedia = ref([]);
$fetch('/data/personal-info.json').then(res => {
    personal.value = res.information;
    socialMedia.value = res.socialMedia;
});


</script>

<template>
    <div class="rounded-3xl z-20 max-lg:mt-8">
        <div class="bg-white sticky top-0 px-6 max-xl:px-2 rounded-3xl py-10">
            <figure class="w-44 h-44 overflow-hidden m-auto rounded-[1.5rem]">
                <img src="/images/MehrabEsmailnia.jpeg" class="w-full h-full object-cover" alt="Mehrab Esmailnia">
            </figure>
            <h1 class="text-center text-primary-active p-4 font-black text-xl">{{personal.fullname}}</h1>
            <div class="text-[.82rem] font-light text-center grid justify-center">
                <span class="bg-[#f6f6f6] text-primary-active rounded-xl py-3 px-8">{{personal.jobTitle}}</span>
            </div>
            <div class="bg-light mt-6 rounded-3xl">
                <div class="grid grid-cols-[repeat(auto-fit,minmax(2rem,auto))] px-10 gap-4 justify-center h-20 items-center">
                    <a v-for="(item , index) in socialMedia" :key="index" :href="item.url" target="_blank" class="bg-primary-active w-8 h-8 rounded-[.5rem] grid items-center justify-center">
                        <i :class="[`fi ${item.icon} text-white flex`]"></i>
                    </a>
                </div>
                <ul class="px-10 max-xl:px-6 grid gap-2 text-md font-light text-primary-active">
                    <li class="grid truncate gap-2 h-8 justify-start items-center grid-cols-[auto_auto]">
                        <div class="grid items-center">
                            <i class="fi fi-rr-calendar-lines text-xl flex"></i>
                        </div>
                        <span>{{personal.birthday}}</span>
                    </li>
                    <li class="grid gap-2 h-8 justify-start items-center grid-cols-[auto_auto]">
                        <div class="grid items-center">
                            <i class="fi fi-rr-visit flex text-xl"></i>
                        </div>
                        <span>{{personal.Location}}</span>
                    </li>
                    <li class="grid gap-2 h-8 justify-start items-center grid-cols-[auto_auto]">
                        <div class="grid items-center">
                            <i class="fi fi-rr-envelope flex text-xl"></i>
                        </div>
                        <span>{{personal.email}}</span>
                    </li>
                    <li class="grid gap-2 h-8 justify-start items-center grid-cols-[auto_auto]">
                        <div class="grid items-center">
                            <i class="fi fi-rr-phone-call flex text-xl"></i>
                        </div>
                        <span>{{ personal.phone }}</span>
                    </li>
                </ul>
                <div class="grid justify-center py-5">
                    <a :href="personal.fileResume" download="MehrabEsmailnia" class="bg-primary-active text-sm text-light font-semibold shadow-xl shadow-primary-medium/40 px-12 rounded-full py-3">
                        <span>Download resume</span>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>