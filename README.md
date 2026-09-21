<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anna Arts | Tours & Art</title>
    
    <link rel="stylesheet" href="Main.css">
    <script src="https://cdn.tailwindcss.com"></script>
    
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">
    
    <!-- Библиотека для генерации QR-кодов AR -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        html { scroll-behavior: smooth; }
        body { background-color: #f9fafb; }
        select {
            appearance: none;
            background-image: url("data:image/svg+xml;charset=US-ASCII,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%22292.4%22%20height%3D%22292.4%22%3E%3Cpath%20fill%3D%22%23000000%22%20d%3D%22M287%2069.4a17.6%2017.6%200%200%200-13-5.4H18.4c-5%200-9.3%201.8-12.9%205.4A17.6%2017.6%200%200%200%200%2082.2c0%205%201.8%209.3%205.4%2012.9l128%20127.9c3.6%203.6%207.8%205.4%2012.8%205.4s9.2-1.8%2012.8-5.4L287%2095c3.5-3.5%205.4-7.8%205.4-12.8%200-5-1.9-9.2-5.5-12.8z%22%2F%3E%3C%2Fsvg%3E");
            background-repeat: no-repeat;
            background-position: right .7em top 50%;
            background-size: .65em auto;
        }
        input[type="color"] {
            appearance: none;
            background-color: transparent;
            border: none;
            padding: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        input[type="color"]::-webkit-color-swatch-wrapper { padding: 0; }
        input[type="color"]::-webkit-color-swatch { border: none; border-radius: 50%; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    </style>
</head>

<body class="antialiased text-black relative">

    <!-- НАВИГАЦИЯ -->
    <nav class="bg-white shadow-sm border-b border-gray-200 sticky top-0 z-40">
        <div class="max-w-[1200px] mx-auto px-4 sm:px-6 py-4 grid grid-cols-3 items-center">
            <div class="justify-self-start">
                <a href="#" class="font-serif text-3xl font-medium text-black whitespace-nowrap">Anna Arts</a>
            </div>
            <div class="hidden md:flex justify-self-center space-x-10 items-center font-sans text-sm tracking-widest uppercase">
                <a href="#about" data-translate="nav_about" class="text-black font-medium hover:opacity-70 transition-opacity">Обо мне</a>
                <a href="#gallery" data-translate="nav_gallery" class="text-black font-medium hover:opacity-70 transition-opacity">Галерея</a>
                <a href="#contact" data-translate="nav_contact" class="text-black font-medium hover:opacity-70 transition-opacity">Контакты</a>
            </div>
            <div class="justify-self-end flex items-center">
                <select id="langSwitcher" class="bg-transparent text-black text-sm font-medium border border-gray-300 rounded-md py-1.5 pl-3 pr-8 focus:outline-none focus:ring-2 focus:ring-black cursor-pointer">
                    <option value="ru" selected>Русский</option>
                    <option value="uk">Українська</option>
                    <option value="fi">Suomi</option>
                    <option value="et">Eesti</option>
                    <option value="no">Norsk</option>
                    <option value="en">English</option>
                    <option value="sv">Svenska</option>
                </select>
            </div>
        </div>
    </nav>

    <main class="max-w-[1200px] mx-auto px-4 sm:px-6 py-12">
        
        <!-- СЕКЦИЯ «ОБО МНЕ» -->
        <section id="about" class="mb-20 bg-white border border-gray-100 rounded-2xl p-8 sm:p-12 shadow-sm">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
                
                <!-- Фото художника -->
                <div class="lg:col-span-5 relative">
                    <div class="aspect-[4/5] rounded-xl overflow-hidden shadow-md bg-gray-100">
                        <img src="https://scontent-hel3-1.xx.fbcdn.net/v/t39.30808-6/733505722_3578597402288239_186323483352222950_n.jpg?stp=dst-jpg_tt6&cstp=mx2043x2048&ctp=s2043x2048&_nc_cat=106&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=GQKa90favI4Q7kNvwFe12xW&_nc_oc=Adr6JEwZvncF760nBywRYmjZyOmFp_SSUSCO4gfPNngfi2xFrGUCTf4kzoVzUQGTtIQDsulyKxd6uvktiWa0eM6Z&_nc_zt=23&_nc_ht=scontent-hel3-1.xx&_nc_gid=3LN1cByCjYnK1FM4BNPDmw&_nc_ss=7b289&oh=00_AQJ3EZlrigJyTYse7UKw6DltP3Y_kxrstox7pcpgKblGfA&oe=6AB6FA23" alt="Анна за работой" class="w-full h-full object-cover">
                    </div>
                    <div class="absolute -bottom-4 -right-4 bg-black text-white px-6 py-4 rounded-xl shadow-lg hidden sm:block">
                        <p class="font-serif text-lg font-medium">Anna Arts</p>
                        <p class="text-xs text-gray-400 uppercase tracking-widest" data-translate="artist_role">Contemporary Artist</p>
                    </div>
                </div>

                <!-- Текстовая информация -->
                <div class="lg:col-span-7 flex flex-col justify-center">
                    <span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-3" data-translate="about_subtitle">О художнике</span>
                    <h2 class="font-serif text-3xl sm:text-4xl font-medium text-black mb-6 leading-snug" data-translate="about_title">Искусство как отражение северной природы и эмоций</h2>
                    
                    <p class="font-sans text-gray-600 text-base leading-relaxed mb-4" data-translate="about_text1">
                        Приветствую! Меня зовут Анна. Я современный художник, живу и создаю свои работы в атмосферных пейзажах Финляндии. Мое творчество вдохновлено суровой красотой севера, глубокими оттенками полярной ночи и сиянием чистых эмоций.
                    </p>
                    
                    <p class="font-sans text-gray-600 text-base leading-relaxed mb-8" data-translate="about_text2">
                        Каждая картина — это уникальная текстурная история, созданная с помощью холста, масла, акрила и авторских техник. Мои работы находятся в частных коллекциях по всей Европе, привнося в интерьеры гармонию, глубину и эстетику современного искусства.
                    </p>

                    <!-- Статистика / Факты -->
                    <div class="grid grid-cols-3 gap-6 pt-6 border-t border-gray-100">
                        <div>
                            <p class="font-serif text-2xl sm:text-3xl font-semibold text-black">6+</p>
                            <p class="text-xs text-gray-500 uppercase tracking-wider mt-1" data-translate="stat_years">Лет опыта</p>
                        </div>
                        <div>
                            <p class="font-serif text-2xl sm:text-3xl font-semibold text-black">100+</p>
                            <p class="text-xs text-gray-500 uppercase tracking-wider mt-1" data-translate="stat_works">Картин создано</p>
                        </div>
                        <div>
                            <p class="font-serif text-2xl sm:text-3xl font-semibold text-black">EU</p>
                            <p class="text-xs text-gray-500 uppercase tracking-wider mt-1" data-translate="stat_delivery">Доставка</p>
                        </div>
                    </div>

                </div>

            </div>
        </section>
        
        <!-- ГАЛЕРЕЯ -->
        <section id="gallery" class="mb-20">
            <div class="text-center mb-12">
                <h2 class="font-serif text-3xl md:text-4xl font-medium mb-3" data-translate="gallery_title">Галерея произведений</h2>
                <p class="text-gray-600 text-sm max-w-xl mx-auto" data-translate="gallery_subtitle">Нажмите на любую картину, чтобы открыть режим виртуальной примерки в интерьере и рассмотреть детали.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Картина 1 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/736x/2c/7c/71/2c7c718aea3dbd176b951b08aac5d7e8.jpg" alt="Северное сияние: Абстракция" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c1_title">Северное сияние: Абстракция</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">450 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c1_desc">Холст, акрил. Глубокие цвета полярной ночи.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 2 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://tse2.mm.bing.net/th/id/OIP.7vDhl1vRDNycvBkXTubppQHaJ-?r=0&rs=1&pid=ImgDetMain&o=7&rm=3" alt="Зимний лес Лапландии" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c2_title">Зимний лес Лапландии</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">680 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c2_desc">Текстурная паста, масло. Отражает дух севера.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 3 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/736x/c6/ad/0a/c6ad0aee9fd5620d060f6487e93014c9.jpg" alt="Полуночное солнце" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c3_title">Полуночное солнце</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">350 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c3_desc">Современное искусство. Идеально для светлых интерьеров.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 4 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://tse1.mm.bing.net/th/id/OIP.0eNwfWJMAxyHKdt00i2UlQHaJ3?r=0&rs=1&pid=ImgDetMain&o=7&rm=3" alt="Арктический рассвет" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c4_title">Арктический рассвет</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">820 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c4_desc">Холст, смешанная техника. Утренние пастельные тона.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 5 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/736x/20/69/9b/20699b35387cb60c18e67109d8280293.jpg" alt="Ледяные узоры" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c5_title">Ледяные узоры</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">500 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c5_desc">Холст, акрил, золотая поталь.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 6 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/736x/99/90/69/99906993766a512f7f006055a3e3dae9.jpg" alt="Тишина фьордов" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c6_title">Тишина фьордов</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">950 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c6_desc">Крупноформатная работа, масло.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 7 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/474x/8e/3d/8b/8e3d8b4646e978ee29b6a44a1e48fd84.jpg" alt="Зимняя геометрия" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c7_title">Зимняя геометрия</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">410 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c7_desc">Минимализм, акрил на холсте.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 8 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/736x/11/93/9a/11939a2dec94421be21daaf78f27f5ae.jpg" alt="Дыхание ветра" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c8_title">Дыхание ветра</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">590 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c8_desc">Текстурная живопись, сдержанные оттенки.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>

                <!-- Картина 9 -->
                <article onclick="openArtModal(this.querySelector('img').src)" class="group cursor-pointer bg-white flex flex-col shadow-sm hover:shadow-xl border border-gray-100 rounded-xl overflow-hidden transition-all duration-300 hover:-translate-y-1.5">
                    <div class="relative overflow-hidden aspect-[4/3] bg-gray-100">
                        <img src="https://i.pinimg.com/736x/18/0d/43/180d4343c6d24aa11d88a8af1770b6c1.jpg" alt="Снежная мгла" class="w-full h-full object-cover transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-white/90 backdrop-blur-sm text-black text-xs font-medium px-2.5 py-1 rounded-full shadow-sm" data-translate="badge_available">В наличии</span>
                    </div>
                    <div class="p-6 flex flex-col flex-grow pointer-events-none">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <h3 class="font-serif text-black text-xl font-medium leading-snug" data-translate="c9_title">Снежная мгла</h3>
                            <span class="text-lg font-semibold text-black bg-gray-50 px-3 py-1 rounded-lg border border-gray-100 flex-shrink-0">730 €</span>
                        </div>
                        <p class="font-sans text-gray-600 text-sm leading-relaxed mb-4 flex-grow" data-translate="c9_desc">Холст, масло. Глубокие переходы серого и синего.</p>
                        <div class="flex items-center text-xs font-semibold text-black uppercase tracking-wider pt-2 border-t border-gray-100">
                            <span data-translate="try_request">Примерить / Запросить &rarr;</span>
                        </div>
                    </div>
                </article>
            </div>
        </section>

        <!-- СЕКЦИЯ ОТЗЫВОВ -->
        <section class="mb-16">
            <div class="flex flex-col items-center justify-center text-center mb-8 gap-4 px-4">
                <div>
                    <h2 class="font-serif text-2xl md:text-3xl font-medium uppercase tracking-wide mb-2" data-translate="reviews_title">Что говорят коллекционеры</h2>
                    <div class="flex items-center justify-center gap-2 text-sm text-gray-700">
                        <div class="flex text-black">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <span class="font-medium" data-translate="reviews_rating">4.8 / 5.0 Средний рейтинг</span>
                    </div>
                </div>

                <!-- Стрелочки прокрутки -->
                <div class="flex items-center gap-2 mt-2">
                    <button onclick="scrollReviews('left')" class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center bg-white hover:bg-gray-100 transition-colors shadow-sm cursor-pointer" aria-label="Назад">
                        <i class="fa-solid fa-chevron-left text-sm"></i>
                    </button>
                    <button onclick="scrollReviews('right')" class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center bg-white hover:bg-gray-100 transition-colors shadow-sm cursor-pointer" aria-label="Вперед">
                        <i class="fa-solid fa-chevron-right text-sm"></i>
                    </button>
                </div>
            </div>

            <div id="reviewsContainer" class="flex gap-6 overflow-x-auto scroll-smooth pb-4 no-scrollbar items-stretch">
                <div class="w-4 sm:w-6 flex-shrink-0"></div>

                <!-- Отзывы с переводами текстов -->
                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev1_title">Потрясающий опыт покупки!</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev1_text">Прекрасное взаимодействие на всех этапах, от первых вопросов до бережной доставки. Картина вживую выглядит еще лучше!</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Мария С.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev2_title">Невероятная атмосфера</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev2_text">Заказывала работу Анны для гостиной. Текстура, цвета и глубина просто завораживают. Интерьер сразу преобразился.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Елена Воронцова</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev3_title">Идеально вошло в интерьер</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev3_text">Очень помогла функция виртуальной примерки на сайте — сразу понял, как размер и рама будут смотреться на стене.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Алексей М.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev4_title">Высокое качество холста</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev4_text">Картина прибыла в идеальном состоянии, упаковано очень надежно. Цвета полностью соответствуют тем, что на экране.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Ольга К.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev5_title">Душа северной природы</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev5_text">Чувствуется невероятная энергетика в каждой детали мазков. Настоящее современное искусство для ценителей.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Johan N.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev6_title">Быстрая доставка</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev6_text">Очень переживал за международную доставку, но все прошло гладко. Картина прилетела в Финляндию за несколько дней.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Markus P.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev7_title">Великолепная работа художника</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev7_text">Анна учла все мои пожелания по кастомизации рамы. Общение было максимально приятным и профессиональным.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Светлана Р.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev8_title">Подарок, который впечатлил</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev8_text">Покупал в подарок для родителей на годовщину. Они в абсолютном восторге от стиля и текстуры!</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Дмитрий Т.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev9_title">Потрясающие переливы цвета</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev9_text">При дневном освещении и при вечерней подсветке картина играет разными красками. Очень красиво.</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Kati L.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="min-w-[300px] sm:min-w-[350px] flex-shrink-0 bg-white p-6 rounded-lg border border-gray-200 shadow-sm flex flex-col justify-between">
                    <div>
                        <i class="fa-solid fa-quote-left text-gray-300 text-2xl mb-2"></i>
                        <h3 class="font-serif font-medium text-lg mb-2" data-translate="rev10_title">Обязательно закажу еще!</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-4" data-translate="rev10_text">Сервис на высоте, всё прозрачно, честно и профессионально. Желаю Анне творческих успехов и вдохновения!</p>
                    </div>
                    <div>
                        <div class="flex text-black text-xs mb-2"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                        <div class="flex items-center justify-between text-xs text-gray-500 border-t pt-3">
                            <span class="font-medium text-black">Игорь В.</span>
                            <span class="flex items-center gap-1 text-green-600"><i class="fa-solid fa-check"></i> <span data-translate="verified">Проверено</span></span>
                        </div>
                    </div>
                </div>

                <div class="w-4 sm:w-6 flex-shrink-0"></div>
            </div>
        </section>

        <!-- СЕКЦИЯ КОНТАКТОВ -->
        <section id="contact" class="bg-white p-8 sm:p-12 rounded-2xl shadow-sm border border-gray-100 max-w-3xl mx-auto mb-12">
            <div class="text-center mb-8">
                <h2 class="font-serif text-3xl font-medium mb-2" data-translate="contact_title">Связаться со мной</h2>
                <p class="text-gray-600 text-sm" data-translate="contact_subtitle">Хотите заказать картину или задать вопрос? Отправьте мне сообщение.</p>
            </div>

            <form id="contactForm" action="https://formspree.io/f/mljdberd" method="POST" class="space-y-6">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-xs font-bold text-gray-500 uppercase mb-2" data-translate="contact_name">Ваше имя</label>
                        <input type="text" name="name" required class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-black text-sm" placeholder="Иван">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-500 uppercase mb-2" data-translate="contact_email">Ваш Email</label>
                        <input type="email" name="email" required class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-black text-sm" placeholder="example@mail.com">
                    </div>
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-500 uppercase mb-2" data-translate="contact_message">Сообщение</label>
                    <textarea name="message" rows="4" required class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-black text-sm" placeholder="Расскажите, какая картина вас интересует..."></textarea>
                </div>
                <button type="submit" class="w-full py-3.5 bg-black text-white font-medium rounded-lg hover:bg-gray-800 transition-colors shadow-sm text-sm uppercase tracking-wider" data-translate="contact_send">
                    Отправить сообщение
                </button>
                <div id="formStatus" class="text-center text-sm hidden font-medium"></div>
            </form>
        </section>

    </main>

    <!-- МОДАЛЬНОЕ ОКНО ПРИМЕРКИ -->
    <div id="artModal" class="fixed inset-0 z-[100] hidden bg-black/90 backdrop-blur-sm flex items-center justify-center p-2 sm:p-4 opacity-0 transition-opacity duration-300">
        <div id="artModalInner" class="bg-white rounded-2xl w-full max-w-5xl h-[90vh] md:h-[85vh] flex flex-col md:flex-row overflow-hidden relative transform scale-95 transition-transform duration-300 shadow-2xl">
            
            <button onclick="closeArtModal()" class="absolute top-4 right-4 z-50 bg-white/90 hover:bg-white backdrop-blur shadow-lg w-10 h-10 rounded-full flex items-center justify-center transition-colors">
                <i class="fa-solid fa-xmark text-xl text-gray-800"></i>
            </button>

            <div id="roomPreview" class="flex-grow relative overflow-hidden flex items-center justify-center">
                <div id="wallBehindArtwork" class="absolute inset-0 z-0 transition-colors duration-300 overflow-hidden">
                    <div id="wallColorLayer" class="absolute inset-0 bg-white"></div>
                    <div id="wallTextureLayer" class="absolute inset-0 z-10" style="mix-blend-mode: multiply; background-repeat: repeat; opacity: 0.85;"></div>
                </div>

                <div id="artworkWrapper" class="relative z-10 transition-all duration-300 flex items-center justify-center p-8">
                    <div class="absolute inset-0 bg-black/30 blur-xl translate-y-4 translate-x-4 rounded pointer-events-none"></div>
                    <img id="previewArtwork" src="" class="relative max-h-[65vh] max-w-[70vw] object-cover rounded-sm transition-all duration-300">
                </div>
            </div>

            <!-- Панель управления примеркой -->
            <div class="w-full md:w-80 lg:w-96 bg-white border-l border-gray-200 p-6 overflow-y-auto flex flex-col gap-6 z-40">
                <div>
                    <button onclick="openArModal()" class="w-full py-2.5 bg-indigo-600 text-white rounded-lg font-medium hover:bg-indigo-700 transition-colors flex items-center justify-center gap-2 shadow-sm text-sm" data-translate="ar_button">
                        <i class="fa-solid fa-qrcode"></i> Посмотреть с телефона (AR)
                    </button>
                </div>

                <div>
                    <h4 class="text-xs font-bold text-gray-400 mb-2 uppercase tracking-wider" data-translate="wall_color">Цвет стены</h4>
                    <div class="flex flex-wrap gap-3 items-center">
                        <button onclick="setWallColor('#ffffff')" class="w-8 h-8 rounded-full shadow-sm border border-gray-300 hover:scale-110 transition-transform" style="background-color: #ffffff;" title="Белый"></button>
                        <button onclick="setWallColor('#d1d5db')" class="w-8 h-8 rounded-full shadow-sm border border-gray-300 hover:scale-110 transition-transform" style="background-color: #d1d5db;" title="Светло-серый"></button>
                        <button onclick="setWallColor('#4b5563')" class="w-8 h-8 rounded-full shadow-sm border border-gray-300 hover:scale-110 transition-transform" style="background-color: #4b5563;" title="Темно-серый"></button>
                        <button onclick="setWallColor('#18181b')" class="w-8 h-8 rounded-full shadow-sm border border-gray-300 hover:scale-110 transition-transform" style="background-color: #18181b;" title="Черный"></button>
                        <div class="relative w-8 h-8 rounded-full shadow-sm border border-gray-300 overflow-hidden hover:scale-110 transition-transform" title="Свой цвет">
                            <input type="color" oninput="setWallColor(this.value)" class="absolute inset-0 w-[150%] h-[150%] -top-1 -left-1 cursor-pointer">
                        </div>
                    </div>
                </div>

                <div>
                    <h4 class="text-xs font-bold text-gray-400 mb-2 uppercase tracking-wider" data-translate="wall_texture">Фактура стены</h4>
                    <div class="grid grid-cols-2 gap-2 text-xs font-medium text-gray-700">
                        <button onclick="setWallTexture('Photos/bk2.png', '400px auto')" class="py-2 px-2 border rounded hover:bg-gray-50 transition-all text-center" data-translate="tex_concrete">Бетон</button>
                        <button onclick="setWallTexture('https://www.transparenttextures.com/patterns/brick-wall.png', '300px auto')" class="py-2 px-2 border rounded hover:bg-gray-50 transition-all text-center" data-translate="tex_brick">Кирпич</button>
                        <button onclick="setWallTexture('https://www.transparenttextures.com/patterns/wood-pattern.png', '300px auto')" class="py-2 px-2 border rounded hover:bg-gray-50 transition-all text-center" data-translate="tex_wood">Дерево</button>
                        <button onclick="setWallTexture('https://www.transparenttextures.com/patterns/plaster-wall.png', '300px auto')" class="py-2 px-2 border rounded hover:bg-gray-50 transition-all text-center" data-translate="tex_plaster">Штукатурка</button>
                        <button onclick="setWallTexture('https://www.transparenttextures.com/patterns/worn-dots.png', '300px auto')" class="py-2 px-2 border rounded hover:bg-gray-50 transition-all text-center" data-translate="tex_canvas">Холст</button>
                        <button onclick="setWallTexture('', '300px auto')" class="py-2 px-2 border rounded hover:bg-gray-100 transition-all text-center" data-translate="tex_smooth">Гладкая</button>
                    </div>
                </div>

                <div>
                    <h4 class="text-xs font-bold text-gray-400 mb-2 uppercase tracking-wider" data-translate="frame_color">Цвет рамки</h4>
                    <div class="flex flex-col gap-2">
                        <div class="flex items-center justify-between px-3 py-2 border rounded bg-gray-50/50 text-xs font-medium text-gray-700">
                            <span data-translate="frame_select">Выберите цвет рамы:</span>
                            <div class="relative w-7 h-7 rounded-full shadow-sm border border-gray-300 overflow-hidden hover:scale-110 transition-transform cursor-pointer">
                                <input type="color" oninput="setCustomColorFrame(this.value)" value="#18181b" class="absolute inset-0 w-[150%] h-[150%] -top-1 -left-1 cursor-pointer">
                            </div>
                        </div>
                        <button onclick="removeFrame()" class="py-1.5 border rounded hover:bg-red-50 text-red-600 text-xs font-medium flex items-center justify-center gap-1.5" data-translate="frame_none">
                            <i class="fa-solid fa-ban"></i>Без рамки
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Модальное окно для AR -->
    <div id="arQrModal" class="fixed inset-0 z-[150] hidden bg-black/80 backdrop-blur-sm flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl p-6 max-w-sm w-full text-center relative shadow-2xl">
            <button onclick="closeArModal()" class="absolute top-3 right-3 text-gray-500 hover:text-black">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            <h3 class="font-serif text-xl font-medium mb-2" data-translate="ar_title">Просмотр в AR</h3>
            <p class="text-sm text-gray-600 mb-4" data-translate="ar_desc">Наведите камеру смартфона, чтобы открыть эту картину</p>
            <div id="qrcodeContainer" class="flex justify-center p-4 bg-gray-50 rounded-xl mb-4 border"></div>
            <p class="text-xs text-gray-400" data-translate="ar_footer">Откроется камера вашего телефона</p>
        </div>
    </div>

    <!-- Подключение скрипта -->
    <script src="script.js"></script>
</body>
</html>
