<h1 align="center">Привет, я Даниил 👋</h1>
<h3 align="center">Fullstack-разработчик | React · TypeScript · Node.js</h3>

<p align="center">
  Проектирую схему БД и REST API с нуля, пишу типизированный код (TypeScript) на фронте и бэке.
  <br/>
  Ниже — готовый проект <a href="https://github.com/Dantul1337/CodeMentor">CodeMentor</a>, полностью рабочий, с деплоем на проде.
</p>

---

### 🔭 Мои проекты

**[CodeMentor](https://github.com/Dantul1337/CodeMentor)** — каталог программистских курсов с формой заявки на обучение, упакованный как устанавливаемое PWA с push-уведомлениями.

- 🎓 REST API на Express: `/api/courses` отдаёт список и карточку курса, `/api/applications` принимает заявки (name/email/phone) — контроллеры и бизнес-логика разделены по паттерну **controller → service → Prisma**
- 📲 Установка приложения без нативного магазина: обработал `beforeinstallprompt` для Chrome/Android и написал отдельный modal-гайд для iOS, где этого события нет вообще — Safari не поддерживает его штатно
- 🔌 Офлайн-режим через кастомный Service Worker на стратегии Workbox `injectManifest` (не готовый плагин "из коробки", а собственный `sw.ts` с точечным кэшированием ассетов)
- 🔔 Push-уведомления в реальном времени: подписки браузеров хранятся в отдельной таблице `PushSubscription`, рассылка идёт через VAPID-подписанный `web-push`, `/api/push/send` шлёт сообщение сразу всем подписчикам
- 🏗️ Три БД-модели (`Course`, `Application`, `PushSubscription`) через Prisma, три независимых сервиса в проде: фронт на Vercel, API на Render, PostgreSQL на Supabase — чтобы деплоить и масштабировать бэкенд отдельно от PWA-оболочки

🔗 Демо: [code-mentor-inky.vercel.app](https://code-mentor-inky.vercel.app/)

---

### 🛠️ Стек технологий

**Frontend:** React 19 + TypeScript (strict) — React Router для клиентского роутинга, Axios для запросов к API, `vite-plugin-pwa` в режиме `injectManifest` для манифеста и кастомного Service Worker
**Backend:** Node.js + Express 5 на TypeScript (`tsx`), Prisma ORM поверх PostgreSQL, `web-push` для VAPID-подписанных push-уведомлений
**Инфраструктура:** Vercel (frontend), Render (backend API), Supabase (managed PostgreSQL) — три отдельных деплоя вместо одного монолита

<p align="left">
  <img src="https://skillicons.dev/icons?i=react,ts,nodejs,express,postgres,prisma,vite,js,html,css,git" alt="Skills" />
</p>

---

### 📊 GitHub статистика

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Dantul1337&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="165"/>
</p>
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
