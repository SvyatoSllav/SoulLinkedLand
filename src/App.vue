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
          <a href="#features" class="text-sm font-medium text-gray-700 hover:text-pink-600">О нас</a>
          <a href="#testimonials" class="text-sm font-medium text-gray-700 hover:text-pink-600">Отзывы</a>
          <a href="#pricing" class="text-sm font-medium text-gray-700 hover:text-pink-600">Цены</a>
          <a href="#contact" class="text-sm font-medium text-gray-700 hover:text-pink-600">Контакты</a>
        </nav>

        <div class="flex items-center gap-4">
          <button class="hidden md:inline-flex h-9 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-4 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600">
            <a href="#pricing">Начать</a>
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
          <a @click="closeMobileMenu" href="#features" class="text-sm font-medium text-gray-700 hover:text-pink-600">О нас</a>
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
          <div class="grid gap-6 lg:grid-cols-[1fr] lg:gap-12 xl:grid-cols-[1fr] justify-center">
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
                  <a href="#pricing">Начать путешествие</a>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-right ml-2 h-4 w-4"><path d="m9 18 6-6-6-6"/></svg>
                </button>
                <button class="inline-flex h-10 items-center justify-center rounded-md border border-gray-200 bg-white px-8 py-2 text-sm font-medium text-gray-900 shadow-sm hover:bg-gray-50">
                  <a href="#features">Узнать больше</a>
                </button>
              </div>
            </div>
<!--            <div class="flex items-center justify-center">-->
<!--&lt;!&ndash;              <img src="./assets/testcouple.jpg" alt="Пара вместе" class="rounded-lg object-cover shadow-lg" />&ndash;&gt;-->
<!--            </div>-->
          </div>
        </div>
      </section>

      <!-- Features Section -->
      <section id="features" class="w-full py-12 md:py-24 lg:py-32 bg-white">
        <div class="container mx-auto px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            <div class="space-y-2">
              <div class="inline-block rounded-lg bg-pink-100 px-3 py-1 text-sm text-pink-600">О нас</div>
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
                <h3 class="text-xl font-bold text-gray-900">Ежедневные методики</h3>
                <p class="text-gray-500">
                  Получите ежедневные методики для отношений, чтобы поддерживать разговор и развивать вашу связь.
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
                  Отслеживайте рост ваших отношений с помощью цифрового дневника, чтобы размышлять о вашем совместном пути.
                </p>
              </div>
            </div>
<!--            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm lg:col-span-3">-->
<!--              <div class="flex flex-col md:flex-row gap-6 items-center">-->
<!--                <div class="md:w-1/2">-->
<!--                  <img src="https://via.placeholder.com/600x400/FFF0F5/FF69B4?text=Превью+Приложения" alt="Приложение SoulLinked" class="rounded-lg shadow-lg" />-->
<!--                </div>-->
<!--                <div class="md:w-1/2 space-y-4">-->
<!--                  <h3 class="text-2xl font-bold text-gray-900">Создано для современных пар</h3>-->
<!--                  <p class="text-gray-500">-->
<!--                    Независимо от того, только ли вы начинаете или вместе уже десятилетия, SoulLinked предоставляет инструменты, которые помогут вам стать ближе. Наше приложение разработано так, чтобы органично вписаться в вашу жизнь, с вопросами от легких до глубоко значимых.-->
<!--                  </p>-->
<!--                  <ul class="space-y-2">-->
<!--                    <li class="flex items-center gap-2">-->
<!--                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>-->
<!--                      <span>Доступно на iOS и Android</span>-->
<!--                    </li>-->
<!--                    <li class="flex items-center gap-2">-->
<!--                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>-->
<!--                      <span>Синхронизация на всех устройствах</span>-->
<!--                    </li>-->
<!--                    <li class="flex items-center gap-2">-->
<!--                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>-->
<!--                      <span>Новые вопросы добавляются еженедельно</span>-->
<!--                    </li>-->
<!--                  </ul>-->
<!--                </div>-->
<!--              </div>-->
<!--            </div>-->
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
                Нас любят
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
                  "Этот сборник полностью преобразил наши отношения. Мы открыли для себя вещи друг о друге, о которых не знали после 5 лет совместной жизни!"
                </blockquote>
                <div class="flex items-center gap-4">
                  <img src="./assets/couple1.png" alt="Аватар" class="h-10 w-10 rounded-full" />
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
                  "Ежедневные упражнения на сближения стали нашей любимой частью дня. Это как маленький импульс для отношений каждое утро!"
                </blockquote>
                <div class="flex items-center gap-4">
                  <img src="./assets/couple2.png" alt="Аватар" class="h-10 w-10 rounded-full" />
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
                  "После 15 лет брака мы думали, что знаем друг о друге всё. Такая коллекция вопросов доказала, что мы чудесно ошибались!"
                </blockquote>
                <div class="flex items-center gap-4">
                  <img src="./assets/couple3.png" alt="Аватар" class="h-10 w-10 rounded-full" />
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
                Выберите план, который подходит для вашего пути отношений.
              </p>
            </div>
          </div>
          <div class="mx-auto grid max-w-5xl gap-6 py-12 lg:grid-cols-3">
            <!-- Basic Plan -->
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm flex flex-col">
              <div class="flex flex-col gap-4">
                <h3 class="text-xl font-bold text-gray-900">Базовый PDF</h3>
                <div class="flex items-baseline gap-1">
                  <span class="text-4xl font-bold text-gray-900">499₽</span>
                  <span class="ml-3 text-2xl font-bold text-gray-400 line-through">799₽</span>
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
              <button @click="buyPDF(1)" class="mt-auto inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 w-full">
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
                  <span class="text-4xl font-bold text-gray-900">999₽</span>
                  <span class="ml-3 text-2xl font-bold text-gray-400 line-through">1399₽</span>
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
              <button @click="buyPDF(2)" class="inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 w-full">
                Купить
              </button>
            </div>

            <!-- Lifetime Plan -->
            <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
              <div class="flex flex-col gap-4">
                <h3 class="text-xl font-bold text-gray-900">Премиум</h3>
                <div class="flex items-baseline gap-1">
                  <span class="text-4xl font-bold text-gray-900">1399₽</span>
                  <span class="ml-3 text-2xl font-bold text-gray-400 line-through">1999₽</span>
                </div>
                <p class="text-gray-500">Для пар, стремящихся к пожизненному росту вместе.</p>
                <ul class="grid gap-2">
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>Все премиум-функции</span>
                  </li>
                  <li class="flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-check-circle h-5 w-5 text-pink-500"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><path d="m9 11 3 3L22 4"/></svg>
                    <span>500+ вопросов для отношений</span>
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
                <button @click="buyPDF(3)" class="mt-auto inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 w-full">
                  Купить
                </button>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="faq" class="w-full py-12 md:py-24 lg:py-32 bg-pink-50">
        <div class="container mx-auto px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            <div class="space-y-2">
              <div class="inline-block rounded-lg bg-pink-100 px-3 py-1 text-sm text-pink-600">Вопросы и ответы</div>
              <h2 class="text-3xl font-bold tracking-tighter md:text-4xl/tight text-gray-900">
                Часто задаваемые вопросы
              </h2>
              <p class="mx-auto max-w-[700px] text-gray-500 md:text-xl">
                Ответы на самые популярные вопросы о нашем сборнике методик для углубления взаимоотношений
              </p>
            </div>
          </div>

          <div class="mx-auto max-w-3xl mt-12">
            <div class="space-y-4">
              <!-- FAQ Item 1 -->
              <div class="rounded-lg border border-gray-200 bg-white">
                <button
                    @click="toggleFaq(0)"
                    class="flex w-full items-center justify-between px-6 py-4 text-left"
                    :aria-expanded="openFaqs[0]"
                    aria-controls="faq-0"
                >
                  <span class="text-lg font-medium text-gray-900">Как использовать сборник вопросов для укрепления отношений?</span>
                  <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-5 w-5 transition-transform"
                      :class="{ 'rotate-180': openFaqs[0] }"
                  >
                    <polyline points="6 9 12 15 18 9"></polyline>
                  </svg>
                </button>
                <div
                    id="faq-0"
                    v-show="openFaqs[0]"
                    class="px-6 pb-4 text-gray-600"
                >
                  <p>Наш сборник вопросов разработан для регулярного использования. Выберите удобное время, когда вы и ваш партнер можете спокойно поговорить без отвлечений. Выбирайте по одному вопросу за раз и обсуждайте его глубоко, давая друг другу возможность полностью выразить свои мысли и чувства. Рекомендуется использовать сборник 1-3 раза в неделю для достижения наилучших результатов в укреплении ваших отношений.</p>
                </div>
              </div>

              <!-- FAQ Item 2 -->
              <div class="rounded-lg border border-gray-200 bg-white">
                <button
                    @click="toggleFaq(1)"
                    class="flex w-full items-center justify-between px-6 py-4 text-left"
                    :aria-expanded="openFaqs[1]"
                    aria-controls="faq-1"
                >
                  <span class="text-lg font-medium text-gray-900">Для каких пар подходит этот сборник вопросов?</span>
                  <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-5 w-5 transition-transform"
                      :class="{ 'rotate-180': openFaqs[1] }"
                  >
                    <polyline points="6 9 12 15 18 9"></polyline>
                  </svg>
                </button>
                <div
                    id="faq-1"
                    v-show="openFaqs[1]"
                    class="px-6 pb-4 text-gray-600"
                >
                  <p>Наш сборник вопросов и методик подходит для пар на любом этапе отношений. Для новых пар это отличный способ глубже узнать друг друга. Для пар, которые вместе уже долгое время, это возможность открыть новые грани отношений и вернуть свежесть чувств. Сборник также полезен для пар, переживающих сложный период, так как помогает восстановить эмоциональную связь и улучшить коммуникацию.</p>
                </div>
              </div>

              <!-- FAQ Item 3 -->
              <div class="rounded-lg border border-gray-200 bg-white">
                <button
                    @click="toggleFaq(2)"
                    class="flex w-full items-center justify-between px-6 py-4 text-left"
                    :aria-expanded="openFaqs[2]"
                    aria-controls="faq-2"
                >
                  <span class="text-lg font-medium text-gray-900">На каких психологических принципах основаны вопросы?</span>
                  <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-5 w-5 transition-transform"
                      :class="{ 'rotate-180': openFaqs[2] }"
                  >
                    <polyline points="6 9 12 15 18 9"></polyline>
                  </svg>
                </button>
                <div
                    id="faq-2"
                    v-show="openFaqs[2]"
                    class="px-6 pb-4 text-gray-600"
                >
                  <p>Наши вопросы и методики разработаны на основе современных психологических исследований в области отношений и эмоциональной близости. Мы опираемся на работы известных психологов, таких как Джон Готтман, Сью Джонсон и Эстер Перель. Вопросы структурированы по категориям, включая эмоциональную близость, коммуникацию, разрешение конфликтов, интимность, совместные цели и ценности. Каждый вопрос тщательно продуман, чтобы стимулировать глубокие и значимые разговоры.</p>
                </div>
              </div>

              <!-- FAQ Item 4 -->
              <div class="rounded-lg border border-gray-200 bg-white">
                <button
                    @click="toggleFaq(3)"
                    class="flex w-full items-center justify-between px-6 py-4 text-left"
                    :aria-expanded="openFaqs[3]"
                    aria-controls="faq-3"
                >
                  <span class="text-lg font-medium text-gray-900">Какие темы охватывает сборник вопросов?</span>
                  <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-5 w-5 transition-transform"
                      :class="{ 'rotate-180': openFaqs[3] }"
                  >
                    <polyline points="6 9 12 15 18 9"></polyline>
                  </svg>
                </button>
                <div
                    id="faq-3"
                    v-show="openFaqs[3]"
                    class="px-6 pb-4 text-gray-600"
                >
                  <p>Наш сборник охватывает широкий спектр тем, важных для здоровых и счастливых отношений: детство и формирование личности, мечты и стремления, страхи и уязвимости, любовь и привязанность, интимность и близость, семейные ценности, финансы, карьера и личностный рост, разрешение конфликтов, совместное будущее, хобби и интересы, а также духовность и философия жизни. Вопросы разделены по уровням глубины, от легких до очень глубоких, что позволяет постепенно углублять ваши беседы.</p>
                </div>
              </div>

              <!-- FAQ Item 5 -->
              <div class="rounded-lg border border-gray-200 bg-white">
                <button
                    @click="toggleFaq(4)"
                    class="flex w-full items-center justify-between px-6 py-4 text-left"
                    :aria-expanded="openFaqs[4]"
                    aria-controls="faq-4"
                >
                  <span class="text-lg font-medium text-gray-900">Как часто рекомендуется использовать методики из сборника?</span>
                  <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-5 w-5 transition-transform"
                      :class="{ 'rotate-180': openFaqs[4] }"
                  >
                    <polyline points="6 9 12 15 18 9"></polyline>
                  </svg>
                </button>
                <div
                    id="faq-4"
                    v-show="openFaqs[4]"
                    class="px-6 pb-4 text-gray-600"
                >
                  <p>Для достижения наилучших результатов мы рекомендуем выделять время для глубоких разговоров 1-3 раза в неделю. Однако важно адаптировать частоту под ваш ритм жизни и потребности отношений. Некоторые пары предпочитают выбирать один вопрос в день за ужином, другие устраивают специальные вечера раз в неделю для более глубоких бесед. Главное — регулярность и искренний интерес к ответам партнера. Помните, что качество разговора важнее количества обсужденных вопросов.</p>
                </div>
              </div>

              <!-- FAQ Item 6 -->
              <div class="rounded-lg border border-gray-200 bg-white">
                <button
                    @click="toggleFaq(5)"
                    class="flex w-full items-center justify-between px-6 py-4 text-left"
                    :aria-expanded="openFaqs[5]"
                    aria-controls="faq-5"
                >
                  <span class="text-lg font-medium text-gray-900">Что делать, если некоторые вопросы вызывают дискомфорт?</span>
                  <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-5 w-5 transition-transform"
                      :class="{ 'rotate-180': openFaqs[5] }"
                  >
                    <polyline points="6 9 12 15 18 9"></polyline>
                  </svg>
                </button>
                <div
                    id="faq-5"
                    v-show="openFaqs[5]"
                    class="px-6 pb-4 text-gray-600"
                >
                  <p>Это совершенно нормально, если некоторые вопросы вызывают дискомфорт — они и созданы для того, чтобы выводить вас из зоны комфорта и способствовать росту отношений. Однако важно соблюдать границы друг друга. Если вопрос вызывает слишком сильный дискомфорт, вы всегда можете пропустить его и вернуться к нему позже, когда будете готовы. Создайте безопасное пространство для общения, где каждый может честно сказать "я пока не готов обсуждать это". Помните, что рост происходит на границе комфорта и дискомфорта, но не в зоне травмы.</p>
                </div>
              </div>
            </div>

            <div class="mt-12 text-center">
              <p class="text-gray-600">Не нашли ответ на свой вопрос?</p>
              <a href="#contact-form" class="inline-flex items-center text-pink-600 hover:text-pink-700 mt-2">
                Свяжитесь с нами
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="ml-1 h-4 w-4"><path d="m9 18 6-6-6-6"/></svg>
              </a>
            </div>
          </div>
        </div>
      </section>
    </main>

    <section id="contact-form" class="w-full py-12 md:py-24 lg:py-32 border-t-1">
      <div class="container mx-auto px-4 md:px-6">
        <div class="flex flex-col items-center justify-center space-y-4 text-center">
          <div class="space-y-2">
            <div class="inline-block rounded-lg bg-pink-100 px-3 py-1 text-sm text-pink-600">Контакты</div>
            <h2 class="text-3xl font-bold tracking-tighter md:text-4xl/tight text-gray-900">
              Свяжитесь с нами
            </h2>
            <p class="mx-auto max-w-[700px] text-gray-500 md:text-xl">
              У вас есть вопросы или предложения? Заполните форму ниже, и мы свяжемся с вами в ближайшее время.
            </p>
          </div>
        </div>

        <div class="mx-auto max-w-2xl mt-12">
          <form @submit.prevent="submitForm" class="space-y-6">
            <div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
              <div class="space-y-2">
                <label for="first-name" class="text-sm font-medium text-gray-700">Имя</label>
                <input
                    id="first-name"
                    v-model="contactForm.firstName"
                    type="text"
                    required
                    class="w-full rounded-md border border-gray-300 px-4 py-2 text-gray-900 shadow-sm focus:border-pink-500 focus:ring-pink-500"
                    placeholder="Введите ваше имя"
                />
              </div>
              <div class="space-y-2">
                <label for="last-name" class="text-sm font-medium text-gray-700">Фамилия</label>
                <input
                    id="last-name"
                    v-model="contactForm.lastName"
                    type="text"
                    class="w-full rounded-md border border-gray-300 px-4 py-2 text-gray-900 shadow-sm focus:border-pink-500 focus:ring-pink-500"
                    placeholder="Введите вашу фамилию"
                />
              </div>
            </div>

            <div class="space-y-2">
              <label for="email" class="text-sm font-medium text-gray-700">Электронная почта</label>
              <input
                  id="email"
                  v-model="contactForm.email"
                  type="email"
                  required
                  class="w-full rounded-md border border-gray-300 px-4 py-2 text-gray-900 shadow-sm focus:border-pink-500 focus:ring-pink-500"
                  placeholder="example@mail.ru"
              />
            </div>

            <div class="space-y-2">
              <label for="phone" class="text-sm font-medium text-gray-700">Телефон</label>
              <input
                  id="phone"
                  v-model="contactForm.phone"
                  type="tel"
                  class="w-full rounded-md border border-gray-300 px-4 py-2 text-gray-900 shadow-sm focus:border-pink-500 focus:ring-pink-500"
                  placeholder="+7 (999) 123-45-67"
              />
            </div>

            <div class="space-y-2">
              <label for="subject" class="text-sm font-medium text-gray-700">Тема</label>
              <select
                  id="subject"
                  v-model="contactForm.subject"
                  required
                  class="w-full rounded-md border border-gray-300 px-4 py-2 text-gray-900 shadow-sm focus:border-pink-500 focus:ring-pink-500"
              >
                <option value="" disabled selected>Выберите тему</option>
                <option value="general">Общий вопрос</option>
                <option value="support">Техническая поддержка</option>
                <option value="billing">Вопросы оплаты</option>
                <option value="partnership">Сотрудничество</option>
                <option value="other">Другое</option>
              </select>
            </div>

            <div class="space-y-2">
              <label for="message" class="text-sm font-medium text-gray-700">Сообщение</label>
              <textarea
                  id="message"
                  v-model="contactForm.message"
                  rows="5"
                  required
                  class="w-full rounded-md border border-gray-300 px-4 py-2 text-gray-900 shadow-sm focus:border-pink-500 focus:ring-pink-500"
                  placeholder="Напишите ваше сообщение здесь..."
              ></textarea>
            </div>

            <div class="flex items-center">
              <input
                  id="privacy-policy"
                  v-model="contactForm.privacyPolicy"
                  type="checkbox"
                  required
                  class="h-4 w-4 rounded border-gray-300 text-pink-600 focus:ring-pink-500"
              />
              <label for="privacy-policy" class="ml-2 text-sm text-gray-700">
                Я согласен с <a href="#" class="text-pink-600 hover:underline">политикой конфиденциальности</a>
              </label>
            </div>

            <div class="flex justify-center">
              <button
                  type="submit"
                  class="inline-flex h-10 items-center justify-center rounded-md bg-gradient-to-r from-red-500 to-pink-500 px-8 py-2 text-sm font-medium text-white shadow hover:from-red-600 hover:to-pink-600 min-w-[200px]"
                  :disabled="formSubmitting"
              >
                <span v-if="formSubmitting">Отправка...</span>
                <span v-else>Отправить сообщение</span>
              </button>
            </div>

            <div v-if="formSubmitted" class="text-center p-4 rounded-md bg-green-50 text-green-700">
              Спасибо за ваше сообщение! Мы свяжемся с вами в ближайшее время.
            </div>
          </form>
        </div>
      </div>
    </section>

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
                О нас
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
      mobileMenuOpen: false,
      formSubmitting: false,
      formSubmitted: false,
      contactForm: {
        firstName: '',
        lastName: '',
        email: '',
        phone: '',
        subject: '',
        message: '',
        privacyPolicy: false
      },
      openFaqs: [false, false, false, false, false, false], // Array to track open/closed state of FAQs
    }
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    },
    closeMobileMenu() {
      this.mobileMenuOpen = false
    },
    submitForm() {
      this.formSubmitting = true;

      // Simulate form submission with a timeout
      setTimeout(() => {
        this.formSubmitting = false;
        this.formSubmitted = true;

        // Reset form after submission
        this.contactForm = {
          firstName: '',
          lastName: '',
          email: '',
          phone: '',
          subject: '',
          message: '',
          privacyPolicy: false
        };

        // Hide success message after 5 seconds
        setTimeout(() => {
          this.formSubmitted = false;
        }, 5000);
      }, 1500);
    },
    toggleFaq(index) {
      // Create a new array to avoid mutating the original directly
      const newOpenFaqs = [...this.openFaqs];
      newOpenFaqs[index] = !newOpenFaqs[index];
      this.openFaqs = newOpenFaqs;
    },
    buyPDF(index) {
      if (index === 1) {
        window.open('https://www.digiseller.market/asp2/pay_wm.asp?id_d=5121276&lang=ru-RU', '_blank', 'noopener')
      }
      if (index === 2) {
        window.open('https://www.digiseller.market/asp2/pay_wm.asp?id_d=5121023&lang=ru-RU', '_blank', 'noopener')
      }
      if (index === 3) {
        window.open('https://www.digiseller.market/asp2/pay_wm.asp?id_d=5121280&lang=ru-RU', '_blank', 'noopener')
      }

    }
  }
}
</script>

<style>


html {
  scroll-behavior: smooth;
}
</style>