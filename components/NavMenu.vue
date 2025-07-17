<template>
    <div class="flex flex-row items-center justify-start fixed page_padding py-4 w-full z-[999] select-none backdrop_filter">
        <p @click="navigateTo('/')" class="text-2xl max-md:text-xl font-semibold cursor-pointer">ShareProject</p>
        <div class="mx-auto flex flex-row items-center justify-center gap-12 max-lg:!hidden">
            <a href="/" class="hover:opacity-80 cursor-pointer">Главная</a>
            <a href="/about" class="hover:opacity-80 cursor-pointer">О нас</a>
            <a href="/contacts" class="hover:opacity-80 cursor-pointer">Контакты</a>
            <a href="/more" class="hover:opacity-80 cursor-pointer">Еще</a>
        </div>
        <div class="flex flex-row items-center justify-center gap-6 max-lg:ml-auto">
            <a href="/account" class="hover:opacity-80 cursor-pointer flex items-center max-md:!hidden">
                <Icon name="mdi:account" size="32" />
            </a>
            <GradientButton @click="navigateTo('/signup')">Регистрация</GradientButton>
        </div>
    </div>
</template>

<style scoped>
    .backdrop_filter {
        background: linear-gradient(180deg,#0f0f0f,#0f0f0f00);
    }
</style>