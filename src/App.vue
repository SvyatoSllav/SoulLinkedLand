<template>
  <div class="min-h-screen flex flex-col">
    <!-- Header -->
    <header class="sticky top-0 z-50 w-full border-b bg-white/95 backdrop-blur supports-[backdrop-filter]:bg-white/60">
      <div class="container mx-auto flex h-16 items-center justify-between px-4">
        <div class="flex items-center gap-2">
          <div class="h-10 w-10 rounded-full bg-gradient-to-r  flex items-center justify-center text-white font-bold"><img src="./assets/jigsaw.png"/></div>
          <span class="text-xl font-bold text-gray-900">SoulLinked</span>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex gap-6">
          <a href="#features" class="text-sm font-medium text-gray-700 hover:text-pink-600">Возможности</a>
          <a href="#testimonials" class="text-sm font-medium text-gray-700 hover:text-pink-600">Отзывы</a>
          <a href="#pricing" class="text-sm font-medium text-gray-700 hover:text-pink-600">Цены</a>
          <a href="#contact" class="text-sm font-medium text-gray-700 hover:text-pink-600">Контакты</a>
        </nav>

        <div class="flex items-center gap-4">
          <button class="hidden md:inline-flex h-9 items-center justify-center rounded-md bg-white px-4 py-2 text-sm font-medium text-gray-900 shadow-sm border border-gray-200 hover:bg-gray-50">
            Войти
          </button>
          <button class="hidden md:inline-flex h-9 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-4 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600">
            Начать
          </button>

          <!-- Mobile Menu Button -->
          <button @click="toggleMobileMenu" class="md:hidden inline-flex h-10 w-10 items-center justify-center rounded-md text-gray-700">
            <svg v-if="!mobileMenuOpen" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-menu"><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
            <svg v-else xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-x"><path d="M18 6 6 18"/><path d="m6 6 12 12"/></svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="mobileMenuOpen" class="md:hidden border-t">
        <nav class="flex flex-col p-4 space-y-4 bg-white">
          <a @click="closeMobileMenu" href="#features" class="text-sm font-medium text-gray-700 hover:text-pink-600">Возможности</a>
          <a @click="closeMobileMenu" href="#testimonials" class="text-sm font-medium text-gray-700 hover:text-pink-600">Отзывы</a>
          <a @click="closeMobileMenu" href="#pricing" class="text-sm font-medium text-gray-700 hover:text-pink-600">Цены</a>
          <a @click="closeMobileMenu" href="#contact" class="text-sm font-medium text-gray-700 hover:text-pink-600">Контакты</a>
          <button class="w-full h-9 items-center justify-center rounded-md bg-white px-4 py-2 text-sm font-medium text-gray-900 shadow-sm border border-gray-200 hover:bg-gray-50">
            Войти
          </button>
          <button class="w-full h-9 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-4 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600">
            Начать
          </button>
        </nav>
      </div>
    </header>

    <main class="flex-1">
      <!-- Hero Section -->
      <section class="w-full py-12 md:py-24 lg:py-32 xl:py-48 bg-gradient-to-br from-pink-50 to-red-50">
        <div class="container mx-auto px-4 md:px-6">
          <div class="grid gap-6 lg:grid-cols-[1fr_400px] lg:gap-12 xl:grid-cols-[1fr_600px]">
            <div class="flex flex-col justify-center space-y-4">
              <div class="space-y-2">
                <h1 class="text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none text-gray-900">
                  Укрепляйте ваши отношения шаг за шагом
                </h1>
                <p class="max-w-[600px] text-gray-500 md:text-xl">
                  Откройте для себя глубокие беседы и укрепите вашу связь с партнером с помощью наших тщательно подобранных вопросов.
                </p>
              </div>
              <div class="flex flex-col gap-2 min-[400px]:flex-row">
                <button class="inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600">
                  Начать путешествие
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-right ml-2 h-4 w-4"><path d="m9 18 6-6-6-6"/></svg>
                </button>
                <button class="inline-flex h-10 items-center justify-center rounded-md border border-gray-200 bg-white px-8 py-2 text-sm font-medium text-gray-900 shadow-sm hover:bg-gray-50">
                  Узнать больше
                </button>
              </div>
              <div class="flex items-center space-x-2 text-sm">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle-2 h-4 w-4 text-pink-500"><path d="M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10z"/><path d="m9 12 2 2 4-4"/></svg>
                <span>7-дневный бесплатный период, без кредитной карты</span>
              </div>
            </div>
            <div class="flex items-center justify-center">
              <img src="https://via.placeholder.com/550x400/FFF0F5/FF69B4?text=Пара+Вместе" alt="Пара вместе" class="rounded-lg object-cover shadow-lg" />
            </div>
          </div>
        </div>
      </section>

      <!-- Features Section -->
      <section id="features" class="w-full py-12 md:py-24 lg:py-32 bg-white">
        <div class="container mx-auto px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            <div class="space-y-2">
              <div class="inline-block rounded-lg bg-pink-100 px-3 py-1 text-sm text-pink-600">Возможности</div>
              <h2 class="text-3xl font-bold tracking-tighter md:text-4xl/tight text-gray-900">
                Создано для углубления вашей связи
              </h2>
              <p class="mx-auto max-w-[700px] text-gray-500 md:text-xl">
                Наши тщательно продуманные вопросы помогают парам исследовать новые грани своих отношений.
              </p>
            </div>
          </div>
          <div class="mx-auto grid max-w-5xl items-center gap-6 py-12 lg:grid-cols-3 lg:gap-12">
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-3 text-center items-center">
                <div class="flex h-12 w-12 items-center justify-center rounded-full bg-pink-100">
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-heart text-pink-500"><path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5l7 7Z"/></svg>
                </div>
                <h3 class="text-xl font-bold text-gray-900">Продуманные вопросы</h3>
                <p class="text-gray-500">
                  Более 1000 тщательно подобранных вопросов, разработанных экспертами по отношениям для стимулирования значимых бесед.
                </p>
              </div>
            </div>
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-3 text-center items-center">
                <div class="flex h-12 w-12 items-center justify-center rounded-full bg-red-100">
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-calendar-heart text-red-500"><path d="M21 10V6a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h8"/><path d="M16 2v4"/><path d="M8 2v4"/><path d="M3 10h18"/><path d="M21.29 17.7a2.43 2.43 0 0 0-2.65-.52c-.3.12-.57.3-.8.53l-.34.34-.35-.34a2.43 2.43 0 0 0-2.65-.53c-.3.12-.56.3-.79.53-.95.94-1 2.53.2 3.74L17.5 24l3.6-3.55c1.2-1.21 1.14-2.8.19-3.74Z"/></svg>
                </div>
                <h3 class="text-xl font-bold text-gray-900">Ежедневные подсказки</h3>
                <p class="text-gray-500">
                  Получайте ежедневные подсказки для отношений, чтобы поддерживать разговор и развивать вашу связь.
                </p>
              </div>
            </div>
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-3 text-center items-center">
                <div class="flex h-12 w-12 items-center justify-center rounded-full bg-pink-100">
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-book-heart text-pink-500"><path d="M4 19.5v-15A2.5 2.5 0 0 1 6.5 2H20v20H6.5a2.5 2.5 0 0 1 0-5H20"/><path d="M16 8.2c0 2.3-3 2.8-3 2.8s-3-.5-3-2.8c0-1.8 1.5-2.7 3-1.2 1.5-1.5 3-.6 3 1.2z"/></svg>
                </div>
                <h3 class="text-xl font-bold text-gray-900">Дневник отношений</h3>
                <p class="text-gray-500">
                  Отслеживайте рост ваших отношений с помощью нашего цифрового дневника, чтобы размышлять о вашем совместном пути.
                </p>
              </div>
            </div>
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm lg:col-span-3">
              <div class="flex flex-col md:flex-row gap-6 items-center">
                <div class="md:w-1/2">
                  <img src="https://via.placeholder.com/600x400/FFF0F5/FF69B4?text=Превью+Приложения" alt="Приложение SoulLinked" class="rounded-lg shadow-lg" />
                </div>
                <div class="md:w-1/2 space-y-4">
                  <h3 class="text-2xl font-bold text-gray-900">Создано для современных пар</h3>
                  <p class="text-gray-500">
                    Независимо от того, только ли вы начинаете или вместе уже десятилетия, SoulLinked предоставляет инструменты, которые помогут вам стать ближе. Наше приложение разработано так, чтобы органично вписаться в вашу жизнь, с вопросами от легких до глубоко значимых.
                  </p>
                  <ul class="space-y-2">
                    <li class="flex items-center gap-2">
                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                      <span>Доступно на iOS и Android</span>
                    </li>
                    <li class="flex items-center gap-2">
                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                      <span>Синхронизация на всех устройствах</span>
                    </li>
                    <li class="flex items-center gap-2">
                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                      <span>Новые вопросы добавляются еженедельно</span>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Testimonials Section -->
      <section id="testimonials" class="w-full py-12 md:py-24 lg:py-32 bg-pink-50">
        <div class="container mx-auto px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            <div class="space-y-2">
              <div class="inline-block rounded-lg bg-pink-100 px-3 py-1 text-sm text-pink-600">Отзывы</div>
              <h2 class="text-3xl font-bold tracking-tighter md:text-4xl/tight text-gray-900">
                Любимо парами повсюду
              </h2>
              <p class="mx-auto max-w-[700px] text-gray-500 md:text-xl">
                Послушайте пары, которые преобразили свои отношения с SoulLinked.
              </p>
            </div>
          </div>
          <div class="mx-auto grid max-w-5xl gap-6 py-12 lg:grid-cols-3">
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-4">
                <div class="flex gap-1">
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                </div>
                <blockquote class="text-lg font-semibold text-gray-900">
                  "SoulLinked полностью преобразило наши отношения. Мы открыли для себя вещи друг о друге, о которых не знали после 5 лет совместной жизни!"
                </blockquote>
                <div class="flex items-center gap-4">
                  <img src="https://via.placeholder.com/40x40/FFF0F5/FF69B4?text=Ю" alt="Аватар" class="h-10 w-10 rounded-full" />
                  <div>
                    <div class="font-medium text-gray-900">Юлия и Максим</div>
                    <div class="text-sm text-gray-500">Вместе 5 лет</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-4">
                <div class="flex gap-1">
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                </div>
                <blockquote class="text-lg font-semibold text-gray-900">
                  "Ежедневные подсказки стали нашей любимой частью дня. Это как маленький импульс для отношений каждое утро!"
                </blockquote>
                <div class="flex items-center gap-4">
                  <img src="https://via.placeholder.com/40x40/FFF0F5/FF69B4?text=А" alt="Аватар" class="h-10 w-10 rounded-full" />
                  <div>
                    <div class="font-medium text-gray-900">Алексей и Яна</div>
                    <div class="text-sm text-gray-500">Вместе 2 года</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-4">
                <div class="flex gap-1">
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFC107" stroke="none"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                </div>
                <blockquote class="text-lg font-semibold text-gray-900">
                  "После 15 лет брака мы думали, что знаем друг о друге всё. SoulLinked доказало, что мы чудесно ошибались!"
                </blockquote>
                <div class="flex items-center gap-4">
                  <img src="https://via.placeholder.com/40x40/FFF0F5/FF69B4?text=Р" alt="Аватар" class="h-10 w-10 rounded-full" />
                  <div>
                    <div class="font-medium text-gray-900">Роман и Мария</div>
                    <div class="text-sm text-gray-500">В браке 15 лет</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Pricing Section -->
      <section id="pricing" class="w-full py-12 md:py-24 lg:py-32 bg-white">
        <div class="container mx-auto px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            <div class="space-y-2">
              <div class="inline-block rounded-lg bg-pink-100 px-3 py-1 text-sm text-pink-600">Цены</div>
              <h2 class="text-3xl font-bold tracking-tighter md:text-4xl/tight text-gray-900">
                Простые, прозрачные цены
              </h2>
              <p class="mx-auto max-w-[700px] text-gray-500 md:text-xl">
                Выберите план, который подходит для вашего пути отношений. Все планы включают 7-дневный бесплатный период.
              </p>
            </div>
          </div>
          <div class="mx-auto grid max-w-5xl gap-6 py-12 lg:grid-cols-3">
            <!-- Basic Plan -->
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm flex flex-col">
              <div class="flex flex-col gap-4">
                <h3 class="text-xl font-bold text-gray-900">Базовый PDF</h3>
                <div class="flex items-baseline gap-1">
                  <span class="text-3xl font-bold text-gray-900">499₽</span>
                </div>
                <p class="text-gray-500">Идеально для пар, только начинающих свой совместный путь.</p>
                <ul class="grid gap-2">
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>350+ вопросов для отношений</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500 shrink-0"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Вопросы прошедшие строгую проверку семейными псхологами</span>
                  </li>
                </ul>
              </div>
              <button class="mt-auto inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 w-full">
                Купить
              </button>
            </div>

            <!-- Premium Plan -->
            <div class="rounded-lg border-2 border-pink-500 bg-white p-6 shadow-md relative flex flex-col justify-between">
              <div class="absolute -top-3 left-1/2 transform -translate-x-1/2 bg-gradient-to-r from-red-500 to-pink-500 text-white text-xs font-bold px-3 py-1 rounded-full">
                Популярный
              </div>
              <div class="flex flex-col gap-4">
                <h3 class="text-xl font-bold text-gray-900">Полный пакет</h3>
                <div class="flex items-baseline gap-1">
                  <span class="text-3xl font-bold text-gray-900">1399₽</span>
                </div>
                <p class="text-gray-500">Для пар, стремящихся углубить свою связь.</p>
                <ul class="grid gap-2">
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>350+ вопросов для отношений</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="shrink-0 lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Психотерапевтические методики для углубления связи</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="shrink-0 lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Рекомендуемая литература для построения крепких и глубоких взаимоотношений</span>
                  </li>
                </ul>
              </div>
              <button class="inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 w-full">
                Купить
              </button>
            </div>

            <!-- Lifetime Plan -->
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-4">
                <h3 class="text-xl font-bold text-gray-900">Премиум</h3>
                <div class="flex items-baseline gap-1">
                  <span class="text-3xl font-bold text-gray-900">1799₽</span>
                </div>
                <p class="text-gray-500">Для пар, стремящихся к пожизненному росту вместе.</p>
                <ul class="grid gap-2">
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Все премиум-функции</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>1000+ вопросов для отношений</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Эксклюзивные семинары для пар</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Приоритетная поддержка</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Все будущие обновления</span>
                  </li>
                </ul>
                <button class="mt-auto inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 w-full">
                  Купить
                </button>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="w-full border-t bg-white">
      <div class="container mx-auto flex flex-col gap-8 py-8 md:py-12 lg:py-16 px-4 md:px-6">
        <div class="grid gap-8 sm:grid-cols-2 md:grid-cols-4">
          <div class="space-y-4">
            <div class="flex items-center gap-2">
              <div class="h-10 w-10 rounded-full bg-gradient-to-r  flex items-center justify-center text-white font-bold"><img src="./assets/jigsaw.png"/></div>
              <span class="text-xl font-bold text-gray-900">SoulLinked</span>
            </div>
            <p class="text-sm text-gray-500">
              Укрепляем отношения с 2023 года.
            </p>
            <div class="flex gap-4">
              <a href="#" class="text-gray-500 hover:text-pink-500">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-twitter h-5 w-5"><path d="M22 4s-.7 2.1-2 3.4c1.6 10-9.4 17.3-18 11.6 2.2.1 4.4-.6 6-2C3 15.5.5 9.6 3 5c2.2 2.6 5.6 4.1 9 4-.9-4.2 4-6.6 7-3.8 1.1 0 3-1.2 3-1.2z"/></svg>
                <span class="sr-only">Twitter</span>
              </a>
              <a href="#" class="text-gray-500 hover:text-pink-500">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-facebook h-5 w-5"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
                <span class="sr-only">Facebook</span>
              </a>
              <a href="#" class="text-gray-500 hover:text-pink-500">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-instagram h-5 w-5"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg>
                <span class="sr-only">Instagram</span>
              </a>
              <a href="#" class="text-gray-500 hover:text-pink-500">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-linkedin h-5 w-5"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
                <span class="sr-only">LinkedIn</span>
              </a>
            </div>
          </div>
          <div class="space-y-4">
            <h3 class="text-sm font-medium text-gray-900">Продукт</h3>
            <nav class="flex flex-col gap-2">
              <a href="#features" class="text-sm text-gray-500 hover:text-pink-500">
                Возможности
              </a>
              <a href="#pricing" class="text-sm text-gray-500 hover:text-pink-500">
                Цены
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Часто задаваемые вопросы
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Скачать приложение
              </a>
            </nav>
          </div>
          <div class="space-y-4">
            <h3 class="text-sm font-medium text-gray-900">Компания</h3>
            <nav class="flex flex-col gap-2">
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                О нас
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Блог
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Карьера
              </a>
              <a href="#contact" class="text-sm text-gray-500 hover:text-pink-500">
                Контакты
              </a>
            </nav>
          </div>
          <div class="space-y-4">
            <h3 class="text-sm font-medium text-gray-900">Юридическая информация</h3>
            <nav class="flex flex-col gap-2">
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Условия использования
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Конфиденциальность
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Файлы cookie
              </a>
              <a href="#" class="text-sm text-gray-500 hover:text-pink-500">
                Лицензии
              </a>
            </nav>
          </div>
        </div>
        <div class="flex flex-col gap-4 sm:flex-row justify-between items-center border-t pt-8">
          <p class="text-xs text-gray-500">
            &copy; 2023 SoulLinked. Все права защищены.
          </p>
          <p class="text-xs text-gray-500">Сделано с ❤️ для пар по всему миру</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'SoulTogetherLanding',
  data() {
    return {
      mobileMenuOpen: false
    }
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    },
    closeMobileMenu() {
      this.mobileMenuOpen = false
    }
  }
}
</script>

<style>


html {
  scroll-behavior: smooth;
}
</style>