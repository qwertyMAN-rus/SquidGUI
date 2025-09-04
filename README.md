# SquidGUI 🦑

**Мощная и элегантная GUI-библиотека для OpenComputers/OpenOS**, построенная на принципах объектно-ориентированного и реактивного программирования. Создавайте сложные интерфейсы с минимальным количеством кода.

![Lua](https://img.shields.io/badge/Made%20with-Lua-blue?logo=lua)
![OpenComputers](https://img.shields.io/badge/For-OpenComputers-orange)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📸 Скриншоты

*[Здесь будет картинка или GIF]*

## ⚡ Быстрый старт

1.  **Скачайте библиотеку...**
2.  **Подключите в вашей программе:**
    ```lua
    local squidgui = require("SquidGUI")
    ```
3.  **Создайте приложение и первое окно:**
    ```lua
    local app = squidgui.Application()
    local window = app:createWindow("Мое окно")
    window:show()
    ```
4.  **Добавьте виджеты в окно**
    ```lua
    local label = squidgui.Label("Привет, мир!")
    local progressBar = squidgui.ProgressBar(0.5)
    local button = squidgui.Button("Обновить прогресс бар")

    window:addWidget(label)
    window:addWidget(progressBar)
    window:addWidget(button)
    ```
5.  **Добавьте логику**
    ```lua
    local function updateProgressBar()
        progressBar.value = math.random()
    end
    button.onClick:addListener(updateProgressBar)
    ```
6. **Запустите код**
    ```lua
    app:run()
    ```

## ✨ Особенности

-   **🎛️ Полностью на ООП:** Чистая архитектура и легко расширяемый код.
-   **⚡ Реактивная модель:** Виджеты автоматически реагируют на изменения данных и действий пользователя.
-   **📁 Управление окнами:** Легко создавайте и управляйте несколькими окнами.
-   **📦 Готовые виджеты:** Встроенный набор популярных компонентов для быстрой разработки.

## 🧩 Виджеты

Библиотека включает в себя следующие стандартные виджеты:

| Виджет | Описание | Пример кода |
| :--- | :--- | :--- |
| **Label** | Текст для отображения | `Label("Мой текст")` |
| **TextButton** | Кнопка с текстом | `TextButton("Нажать", function() print("Клик!") end)` |
| **InputBox** | Поле для ввода одной строки | `InputBox("Place Holder")` |
| **TextBox** | Многострочное поле для ввода | `TextBox("Place Holder")` |
| **Slider** | Ползунок для выбора значения | `Slider(0.5)` -- 50% |
| **ProgressBar** | Индикатор выполнения | `ProgressBar(0.75)` -- 75% |

## 📜 Лицензия

Этот проект распространяется под лицензией MIT. См. файл [LICENSE](LICENSE) для получения подробной информации.

## 🤝 Содействие разработке

Сообщения об ошибках, предложения новых функций и запросы на слияние (pull requests) приветствуются!

---

**Наслаждайтесь созданием интерфейсов с SquidGUI! 🦑**