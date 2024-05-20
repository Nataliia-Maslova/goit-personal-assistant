# Персональний помічник

Цей проект реалізує систему управління контактами та нотатками, що дозволяє користувачам зберігати, шукати, редагувати та видаляти інформацію в персональній адресній книзі та блокноті нотаток.

## Структура проекту

Проект має наступну структуру каталогів та файлів:

- `src/`: Вихідний код програми.
  - `personal_assistant`: Каталог з файлами пакету
    - `commands/`: Обробники cli команд
      - `contact_commands.py`: визначення команд для роботи з контактами
      - `note_commands.py`: визначення команд для роботи з нотатками
    - `models/`: Моделі даних для представлення бізнес-об'єктів.
      - `contact.py`: Клас `Contact` для управління контактами.
      - `email_address.py`: Клас `EmailAddress` для роботи з електронними адресами.
      - `phone_number.py`: Клас `PhoneNumber` для роботи з телефонними номерами.
      - `address.py`: Клас `Address` для роботи з адресами.
      - `birthday.py`: Клас `Birthday` для роботи з датами народження.
      - `note.py`: Клас `Note` для управління нотатками.
      - `tag.py`: Клас `Tag` для тегування нотаток.
    - `enums/`: Перелічувані типи (enums) використовуються у проекті.
      - `entity_type.py`: Enum `EntityType` для визначення типів сутностей.
    - `services/`: Сервіси для логіки обробки даних.
      - `address_book.py`: Сервіс для управління адресною книгою.
      - `notebook.py`: Сервіс для управління нотатками.
      - `storage_service.py`: Сервіс для зберігання та завантаження даних.  
      - `tag_manager.py`: Сервіс для керуванням тегами
    - `utils/`: Утиліти та допоміжні інструменти.
      - `decorators.py`: Декоратори
      - `validators.py`: Валідатори для перевірки вхідних даних.
      - `helpers.py`: Допоміжні функції.
    - `cli.py`: Основний файл CLI інтерфейсу.
    - `main.py`: Основний виконуваний файл для демонстрації використання.
- `data/`: Каталог для збереження даних.
- `requirements.txt`: Файл з залежностями проекту.

## Інсталяція

Для встановлення та запуску проекту виконайте наступні кроки:

1. Клонуйте репозиторій:
   ```bash
   git clone https://github.com/sergyinfo/goit-personal-assistant
   cd goit-personal-assistant
   ```

2. Створіть та активуйте віртуальне середовище:
    ### Для Linux/MacOS:
   ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
    ### Для Windows:
   ```bash
    python -m venv venv
    .\venv\Scripts\activate
    ```

3. Встановіть необхідні залежності:
    ```bash
    pip install -r requirements.txt
    ```

4. Запустіть програму з командного рядка:
    ```bash
    cd src
    python -m personal_assistant
    ```