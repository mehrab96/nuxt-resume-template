<script setup>

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
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-black text-primary-active text-md">Learning C++ programming language</h4>
                    <span class="font-mono font-black text-sm text-primary-active/90">2015-2016</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">My first programming experience was in the DOS environment with C++ language, which I think was a suitable option for learning programming logic, but after several months of practice, I decided to leave the DOS environment and experience Visual Basic.</p>
                </li>
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-semibold ltr:font-black text-primary-active text-md">C# programming language</h4>
                    <span class="ltr:font-mono ltr:font-black text-sm font-semibold text-primary-active/90">2016-2017</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">After the experience of working with Visual Basic, I decided to use C# to deliver my university project, and this made me go with C# for almost a year.</p>
                </li>
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-black text-primary-active text-md">Wordpress</h4>
                    <span class="font-mono font-black text-sm text-primary-active/90">2018-2020</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">After working with C# for a while, I didn' t know much about its business and I couldn't send the projects I was working on. I started learning php with the suggestion of one of my classmates who was familiar with web business. I learned WordPress, entered the job market very quickly and was designing templates and selling subscriptions on websites. After a while, because I was very fond of learning and teaching, I first taught HTML, CSS, and WordPress in one of the schools in my city.</p>
                </li>
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-black text-primary-active text-md">Laravel</h4>
                    <span class="font-mono font-black text-sm text-primary-active/90">2020-2024</span>
                    <p class="font-light text-[.93rem] leading-8 text-primary-active">The business market in WordPress was a very good experience for me, but I didn't feel that it was a new program for me, so with the research I did and again with the suggestion of one of my friends, I started learning Laravel and Start, and because I was familiar with the market, I started designing scripts. I used to do it and sell it as a subscription, and that made me experience exclusive work using Laravel. In order to be a complete programmer (full stack), I continued using one of the javascript frameworks, which was vue js, from the beginning along with Laravel until now.</p>
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
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-semibold ltr:font-black text-primary-active text-md">Mohammad Baqer Sari University</h4>
                    <span class="ltr:font-mono text-sm font-semibold text-primary-active/90">2015-2016</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">Studying in associate degree, software engineering field and starting programming activities</p>
                </li>
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-black text-primary-active text-md">Tabari University</h4>
                    <span class="ltr:font-mono text-sm font-semibold text-primary-active/90">2017-2019</span>
                    <p class="font-light text-[.93rem] leading-8 text-primary-active">Studying in the bachelor's degree in software engineering and starting to work in the web field (designing WordPress templates)</p>
                </li>
                <li class="mb-8 relative circleOverLi">
                    <h4 class="font-black text-primary-active text-md">Tabari University</h4>
                    <span class="font-mono text-sm font-semibold text-primary-active/90">2020-2024</span>
                    <p class="font-extralight ltr:font-light text-[.93rem] leading-8 text-primary-active">Studying for a master's degree in software engineering and continuing to work in the field of websites, designing and developing Lordint's website and online training in the field of web</p>
                </li>
            </ul>
        </div>
    </div>
</NuxtLayout>
</template>