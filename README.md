# 🐂🐄 Бики та Корови — Telegram-бот

![Python](https://img.shields.io/badge/python-3.10+-blue)
![Aiogram / PTB](https://img.shields.io/badge/python--telegram--bot-async-green)
![SQLite](https://img.shields.io/badge/SQLite-DB-lightgrey)
![License](https://img.shields.io/badge/license-MIT-yellow)

---

## 📌 Про проєкт

Telegram-бот класичної логічної гри **«Бики та Корови»**.

Бот загадує 4-значне число з унікальних цифр, а гравець намагається його відгадати.

Проєкт створений як:
- навчальна робота
- приклад асинхронного Python
- демонстрація роботи з Telegram Bot API та SQLite

---

## 🎮 Як грати

- 🐂 **Бик** — цифра на правильній позиції
- 🐄 **Корова** — цифра є, але на іншій позиції

Гравець вводить число та отримує підказки після кожної спроби.

---

## 🚀 Можливості

### 👤 Для гравця:
- Нова гра
- Інтерактивний ввід (inline-клавіатура)
- Історія спроб
- Статистика:
  - кількість ігор
  - перемоги / поразки
  - найкращий результат
- Таблиця лідерів

### 👑 Для адміністратора:
- Перегляд користувачів
- Загальна статистика
- Призначення адмінів (`/promote`)
- Скидання статистики (`/resetstats`)

---

## 🛠 Технології

- Python 3.10+
- python-telegram-bot (async)
- aiosqlite
- SQLite

---

## 📁 Структура бази даних

### users
- id
- telegram_id
- username
- role (player/admin)
- created_at

### games
- id
- telegram_id
- secret
- attempts
- won
- played_at

---

## ▶️ Швидкий старт

### 1. Встановлення залежностей
```bash
pip install -r requirements.txt