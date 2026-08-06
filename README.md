<h1 align="center">Привет, я Даниил 👋</h1>
<h3 align="center">Fullstack-разработчик | React · TypeScript · Node.js</h3>

<p align="center">
  Проектирую схему БД и REST API с нуля, пишу типизированный код (TypeScript) на фронте и бэке.
  <br/>
  Ниже — два готовых проекта, полностью рабочих, с деплоем на проде: <a href="https://github.com/Dantul1337/GroceryExpress">GroceryExpress</a> и <a href="https://github.com/Dantul1337/CodeMentor">CodeMentor</a>,
  а также <a href="https://github.com/Dantul1337/TaskTracker">TaskTracker</a> — бэкенд с упором на покрытие тестами.
</p>

---

### 🔭 Мои проекты

**[GroceryExpress](https://github.com/Dantul1337/GroceryExpress)** — интернет-магазин по доставке продуктов с живым отслеживанием курьера на карте и авто-назначением доставки.

- 🛒 REST API на Express: 7 групп роутов (`auth`, `products`, `orders`, `addresses`, `admin`, `delivery`, `upload`) с тремя независимыми уровнями доступа — свой middleware на покупателя, администратора и курьера
- 💳 Оплата через Stripe Checkout: сервер создаёт Checkout Session, а webhook на `payment_intent.succeeded` списывает товар со склада и запускает фоновые события
- 🤖 Авто-назначение курьера через Inngest: спустя 5 минут после оплаты сервер сам находит свободного курьера, генерирует 6-значный OTP и переводит заказ в статус `Assigned` — без участия администратора
- 🗺️ Живой трекинг доставки: курьер обновляет геопозицию через API, покупатель видит её на карте (React Leaflet) в реальном времени на странице своего заказа
- 🏗️ Пять БД-моделей (`User`, `Address`, `Product`, `Order`, `DeliveryPartner`) через Prisma, три независимых сервиса в проде: фронт на Vercel, API на Render, PostgreSQL на Neon

🔗 Демо: [grocery-express-theta.vercel.app](https://grocery-express-theta.vercel.app/)

---

**[CodeMentor](https://github.com/Dantul1337/CodeMentor)** — каталог программистских курсов с формой заявки на обучение, упакованный как устанавливаемое PWA с push-уведомлениями.

- 🎓 REST API на Express: `/api/courses` отдаёт список и карточку курса, `/api/applications` принимает заявки (name/email/phone) — контроллеры и бизнес-логика разделены по паттерну **controller → service → Prisma**
- 📲 Установка приложения без нативного магазина: обработал `beforeinstallprompt` для Chrome/Android и написал отдельный modal-гайд для iOS, где этого события нет вообще — Safari не поддерживает его штатно
- 🔌 Офлайн-режим через кастомный Service Worker на стратегии Workbox `injectManifest` (не готовый плагин "из коробки", а собственный `sw.ts` с точечным кэшированием ассетов)
- 🔔 Push-уведомления в реальном времени: подписки браузеров хранятся в отдельной таблице `PushSubscription`, рассылка идёт через VAPID-подписанный `web-push`, `/api/push/send` шлёт сообщение сразу всем подписчикам
- 🏗️ Три БД-модели (`Course`, `Application`, `PushSubscription`) через Prisma, три независимых сервиса в проде: фронт на Vercel, API на Render, PostgreSQL на Supabase — чтобы деплоить и масштабировать бэкенд отдельно от PWA-оболочки

🔗 Демо: [code-mentor-inky.vercel.app](https://code-mentor-inky.vercel.app/)

---

**[TaskTracker](https://github.com/Dantul1337/TaskTracker)** — REST API для трекера задач с JWT-аутентификацией, сделанный как демонстрация покрытия бэкенда тестами.

- ✅ Двухуровневое тестирование: юнит-тесты сервисов (`Vitest`, с моками зависимостей) и интеграционные тесты через `Supertest` — реальные HTTP-запросы к `/api/auth` и `/api/tasks`, включая проверку авторизации и доступа к чужим задачам
- 🔐 JWT-аутентификация и хэширование паролей через `bcrypt`, доступ к задачам только у их владельца
- 🏗️ Две БД-модели (`User`, `Task`) через Prisma поверх PostgreSQL, отдельная тестовая база данных, изолированная от рабочей
- 🧱 Архитектура по паттерну **route → controller → service**, типизация на TypeScript

---

### 🛠️ Стек технологий

**Frontend:** React 19 + TypeScript (strict) — React Router для клиентского роутинга, Axios для запросов к API, Tailwind CSS для стилизации, `vite-plugin-pwa` в режиме `injectManifest` для манифеста и кастомного Service Worker
**Backend:** Node.js + Express 5 на TypeScript (`tsx`), Prisma ORM поверх PostgreSQL, Stripe для онлайн-оплаты, Inngest для фоновых и отложенных задач, `web-push` для VAPID-подписанных push-уведомлений
**Инфраструктура:** Vercel (frontend), Render (backend API), Neon и Supabase (managed PostgreSQL) — отдельные деплои вместо одного монолита в каждом проекте
**Тестирование:** Vitest (юнит-тесты) + Supertest (интеграционные тесты API)

<p align="left">
  <img src="https://skillicons.dev/icons?i=react,ts,nodejs,express,postgres,prisma,vite,tailwind,js,html,css,git" alt="Skills" />
</p>

---

### 📊 GitHub статистика

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Dantul1337&theme=tokyo-night&hide_border=true" alt="Activity Graph" />
</p>

---

### 📫 Как со мной связаться

<p align="left">
  <a href="mailto:dantul1337@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://t.me/dantul">
    <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Dantul1337&label=Profile%20views&color=blueviolet&style=flat" alt="Profile views" />
</p>
