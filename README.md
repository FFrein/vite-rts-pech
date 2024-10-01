Вот улучшенная версия вашего README-файла с более красивым и структурированным оформлением:

# React + TypeScript + Vite

0. Создать проект
   ```bash
   yarn create vite Name --template react-ts
   ```
## 🚀 Установка Prettier

[Документация Prettier](https://prettier.io/docs/en/install.html)

1. Сначала установите Prettier локально:
   ```bash
   yarn add --dev --exact prettier
   ```

2. Затем создайте пустой конфигурационный файл, чтобы дать понять редакторам и другим инструментам, что вы используете Prettier:
   ```bash
   node --eval "fs.writeFileSync('.prettierrc','{}\n')"
   ```

3. Создайте файл `.prettierignore`, чтобы указать CLI Prettier и редакторам, какие файлы не следует форматировать. Пример:
   ```bash
   node --eval "fs.writeFileSync('.prettierignore','# Ignore artifacts:\nbuild\ncoverage\n')"
   ```

4. Теперь отформатируйте все файлы с помощью Prettier:
   ```bash
   yarn prettier . --write
   ```

5. Для проверки форматирования выполните:
   ```bash
   npx prettier . --check
   ```

---

## 🧪 ESLint (и другие линтеры)

[Инструкция по установке ESLint](https://github.com/prettier/eslint-config-prettier#installation)

**Примечание:** есть в template react-ts из коробки

---
## ⛰️ Git хуки

1. Установите Husky и lint-staged:
   ```bash
   yarn add --dev husky lint-staged
   ```

2. Инициализируйте Husky:
   ```bash
   npx husky init
   ```

3. Добавьте хук pre-commit:
   ```bash
   node --eval "fs.writeFileSync('.husky/pre-commit','npx lint-staged\n')"
   ```

4. Добавьте следующее в ваш `package.json`:
   ```json
   {
     "husky": {
       "hooks": {
         "pre-commit": "lint-staged"
       }
     }
   }
   ```

5. Установите Husky:
   ```bash
   npx husky install
   ```

> **Примечание:** Если вы видите сообщение "installation deprecated", это нормально.

6. Добавте в package.json lint-staged
    ```bash
   "lint-staged": {
       "**/*": [
         "eslint --fix",
         "prettier --write --ignore-unknown"
       ]
     },
    ```
---
