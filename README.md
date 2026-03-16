# 🎓 My Blog - Проект для студентов

## 👋 Добро пожаловать!

Это учебный проект для практики работы со **Spring Boot**.

Вам предстоит **дописать недостающую функциональность** backend приложения-блога.

**Репозиторий:** https://github.com/Yandex-Practicum/mcrpo-my-blog-pre

---

## 📚 С чего начать?

### 0. Клонируйте проект

```bash
git clone https://github.com/Yandex-Practicum/mcrpo-my-blog-pre.git
cd mcrpo-my-blog-pre
```

### 1. Прочитайте задание

**Откройте файл:** [`ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md`](./ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md)

В нём вы найдёте:
- ✅ Описание задания
- ✅ Пошаговые инструкции
- ✅ Примеры кода
- ✅ Критерии оценки
- ✅ Процесс сдачи работы

### 2. Найдите TODO в коде

```bash
grep -r "TODO:" src/
```

Или откройте [`TODO_TASKS.md`](./TODO_TASKS.md) для краткого списка задач.

### 3. Реализуйте функциональность

Следуйте инструкциям в [`ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md`](./ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md).

### 4. Соберите и проверьте

```bash
# Собрать backend (Executable JAR)
mvn clean package

# Запустить тесты
mvn test

# Запустить backend (встроенный Jetty)
java -jar target/my-blog-back-app.jar
```

---

## 📁 Структура проекта

```
mcrpo-my-blog-pre/
├── src/main/java/com/myblog/
│   ├── config/          # Spring конфигурация
│   ├── controller/      # REST контроллеры (TODO здесь!)
│   ├── service/         # Бизнес-логика (TODO здесь!)
│   ├── dao/             # Работа с БД (TODO здесь!)
│   ├── model/           # Модели данных
│   └── dto/             # Data Transfer Objects
├── src/test/           # Тесты (TODO: дописать)
├── frontend/           # Frontend (React + Vite)
├── pom.xml             # Maven конфигурация
├── ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md  # 📖 НАЧНИТЕ ОТСЮДА!
├── TODO_TASKS.md       # Краткий чек-лист
└── README_СТУДЕНТЫ.md  # Техническая документация
```

---

## 🎯 Что нужно сделать

| Задание | Баллы |
|---------|-------|
| 1. Добавление и удаление лайков | 10 |
| 2. Редактирование и удаление комментариев | 10 |
| 3. Удаление поста (каскадное) | 5 |
| 4. Unit-тесты (БОНУС) | +15 |
| **ИТОГО** | **25-40** |

---

## 🚀 Быстрый старт

```bash
# 1. Клонировать проект
git clone https://github.com/Yandex-Practicum/mcrpo-my-blog-pre.git
cd mcrpo-my-blog-pre

# 2. Собрать backend
mvn clean package

# 3. Запустить backend (встроенный Jetty)
java -jar target/my-blog-back-app.jar

# Backend запустится на http://localhost:8080

# 4. Запустить frontend (в другом терминале, опционально)
# ⚠️ Требуется Node.js 18+ и npm
# Установка: brew install node (macOS) или https://nodejs.org

cd frontend
npm install
npm run dev

# Frontend запустится на http://localhost:3000
# Или тестируйте backend через curl/Postman
```

---

## 🛠 Технологии

- Java 17
- Spring Boot 3.2+
- Maven
- Spring Web (Spring MVC)
- Spring Data JDBC + JdbcTemplate
- H2 Database (in-memory)
- JUnit 5 + Spring Boot Test

---

## 🗄️ H2 Console

После запуска приложения H2 Console доступна по адресу `http://localhost:8080/h2-console`.

Параметры входа (важно указать именно **in-memory** БД, иначе H2 будет пытаться открыть файловую БД вроде `C:/Users/.../test`):

- **JDBC URL**: `jdbc:h2:mem:blogdb`
- **User Name**: `sa`
- **Password**: *(пусто)*

---

## 📖 Документация

- **[ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md](./ЗАДАНИЕ_ДЛЯ_СТУДЕНТОВ.md)** — полное описание задания
- **[TODO_TASKS.md](./TODO_TASKS.md)** — краткий чек-лист
- **[README_СТУДЕНТЫ.md](./README_СТУДЕНТЫ.md)** — техническая документация

---

## ❓ Часто задаваемые вопросы

### Как найти все TODO?

```bash
grep -rn "TODO:" src/
```

### Как запустить только тесты?

```bash
mvn test
```

### Как проверить endpoint через curl?

```bash
curl http://localhost:8080/api/posts/1/likes -X POST
```

### Что делать, если застрял?

1. Прочитайте существующий код — все TODO методы похожи на уже реализованные
2. Читайте логи Jetty — ошибки видны в консоли
3. Смотрите БД через H2 консоль: http://localhost:8080/h2-console

---

## 🎓 Успехов!

**Помните:** Цель не просто сделать, а **научиться**!

Изучайте существующий код, экспериментируйте, задавайте вопросы.

---

**Удачи! 🚀**
