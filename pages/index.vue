<template>
     <div class="flex flex-col w-full h-full min-h-screen relative text-white page_padding">
		<div class="flex flex-col items-center justify-center h-full gap-8 my-auto w-full text-center">
			<h1 class="text-8xl font-bold max-lg:text-6xl max-md:text-5xl">Добро пожаловать в ShareProject</h1>
			<p class="text-2xl max-lg:text-xl max-md:text-base">ShareProject - это платформа для обмена проектами с другими пользователями.</p>
			<button @click="navigateTo('/signup')" class="bg-gradient-to-r from-white to-gray-200 text-black text-xl rounded-xl hover:bg-gradient-to-r hover:from-gray-200 hover:to-gray-200 cursor-pointer px-12 py-6 max-lg:text-lg max-md:text-base max-lg:px-8 max-lg:py-4 max-md:px-6 max-md:py-3">
				Начать сейчас
			</button>
		</div>
        <BackgroundsAstronaut/>
     </div>
     <div class="flex flex-col w-full h-full min-h-screen relative text-white page_padding">
        <div class="flex flex-col items-center justify-center h-full gap-8 w-full text-center my-24">
			<h1 class="text-5xl font-bold max-lg:text-4xl max-md:text-3xl">Здесь реализуются ваши идеи</h1>
			<p class="text-2xl max-lg:text-xl max-md:text-base max-w-4xl">Присоединяйтесь к нам, помогайте другим пользователям, задавайте вопросы - получайте ответы.</p>
			<div class="max-w-4xl mt-8 outline-3 outline-indigo-400 rounded-lg flex items-center justify-center overflow-hidden">
				<video autoplay class="relative bottom-0 left-1/2 z-10 w-auto -translate-x-1/2 overflow-hidden rounded-t-lg" loop muted playsinline preload="auto" src="/assets/video/coding.mp4"></video>
			</div>
			<button @click="navigateTo('/more')" class="mt-4 bg-gradient-to-r from-white to-gray-200 text-black text-lg rounded-full hover:bg-gradient-to-r hover:from-gray-200 hover:to-gray-200 cursor-pointer px-8 py-4 max-lg:text-lg max-md:text-base max-lg:px-8 max-lg:py-4 max-md:px-6 max-md:py-3">
				Узнать больше
			</button>
		</div>
		<WhyUsAndFaq />
		<BackgroundsSpace />
    </div>

</template>
