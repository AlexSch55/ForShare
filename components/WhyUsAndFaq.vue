<template>
  <section class="w-full flex flex-col items-center justify-center py-20 bg-transparent page_padding">
    <div class="w-full max-w-4xl mx-auto">
      <h2 class="text-5xl font-bold text-center text-white mb-4">Частые вопросы</h2>
      <p class="text-lg text-center text-gray-300 mb-10">Здесь вы найдете ответы на самые часто задаваемые вопросы</p>
      <div class="flex flex-col gap-6">
        <div
          v-for="(item, idx) in faqList"
          :key="idx"
          class="w-full bg-black/70 border border-indigo-400 rounded-2xl transition-all duration-300 overflow-hidden"
          :class="{
            'shadow-lg border-indigo-500': openIndex === idx,
            'hover:border-indigo-400': openIndex !== idx
          }"
        >
          <button
            class="flex items-center justify-between w-full px-8 py-6 text-left focus:outline-none select-none cursor-pointer"
            @click="toggle(idx)"
          >
            <span class="flex items-center gap-4">
              <span class="min-w-8 h-8 flex items-center justify-center rounded-full border border-white text-lg text-white font-semibold" :class="{'bg-indigo-400 !border-indigo-300': openIndex === idx}">{{ idx + 1 }}</span>
              <span class="text-xl text-white font-medium">{{ item.q }}</span>
            </span>
            <span class="ml-4">
              <svg v-if="openIndex === idx" width="28" height="28" fill="none" viewBox="0 0 24 24"><path stroke="#a5b4fc" stroke-width="2" stroke-linecap="round" d="M6 12h12"/></svg>
              <svg v-else width="28" height="28" fill="none" viewBox="0 0 24 24"><path stroke="#a5b4fc" stroke-width="2" stroke-linecap="round" d="M12 6v12M6 12h12"/></svg>
            </span>
          </button>
          <transition name="faq-fade">
            <div
              v-show="openIndex === idx"
              class="px-8 pb-6 text-base text-gray-300 transition-all duration-300"
            >
              {{ item.a }}
            </div>
          </transition>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const faqList = [
  {
    q: 'Как опубликовать свой проект на платформе?',
    a: 'Чтобы опубликовать проект, зарегистрируйтесь, перейдите в личный кабинет и нажмите «Добавить проект». Заполните описание, загрузите файлы и выберите уровень доступа.'
  },
  {
    q: 'Кто может просматривать и скачивать мои проекты?',
    a: 'Вы сами выбираете уровень доступа: проект может быть публичным, доступным только по ссылке или приватным для выбранных пользователей.'
  },
  {
    q: 'Могу ли я найти команду или единомышленников для совместной работы?',
    a: 'Да! На платформе есть поиск по интересам, фильтры и система откликов — вы легко найдете людей для совместной работы или обсуждения идей.'
  },
  {
    q: 'Как защитить свои авторские права на проект?',
    a: 'Вы можете указать лицензию при публикации, а также добавить пометку об авторстве. Платформа поддерживает различные типы лицензий и защищает ваши права.'
  },
  {
    q: 'Можно ли делиться не только кодом, но и другими материалами (дизайн, документация)?',
    a: 'Да, вы можете загружать любые файлы: исходники, дизайн-макеты, инструкции, видео и презентации.'
  },
  {
    q: 'Как получить обратную связь или помощь по своему проекту?',
    a: 'Пользователи могут оставлять комментарии, ставить лайки и задавать вопросы. Также вы можете подключить обсуждение или создать отдельную ветку для обратной связи.'
  }
]

const openIndex = ref(0)
const toggle = idx => {
  openIndex.value = openIndex.value === idx ? null : idx
}
</script>

<style scoped>
.faq-fade-enter-active, .faq-fade-leave-active {
  transition: all 0.3s cubic-bezier(.4,0,.2,1);
}
.faq-fade-enter-from, .faq-fade-leave-to {
  opacity: 0;
  max-height: 0;
}
.faq-fade-enter-to, .faq-fade-leave-from {
  opacity: 1;
  max-height: 200px;
}
</style> 