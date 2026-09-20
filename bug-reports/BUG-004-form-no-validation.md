# BUG-004: Форма оформления заказа не валидирует имя и фамилию

**Severity:** Major

**Priority:** High

**User:** standard_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
Форма оформления заказа принимает **невалидные данные** в полях First Name и Last Name. Имя и фамилия должны содержать **только буквы**, но форма принимает **цифры**, **специальные символы** и **пробелы**.

## Test data (классы невалидных данных)
- **Цифры:** `111`, `123`, `999`
- **Спецсимволы:** `!`, `@`, `#`, `$`
- **Пробелы:** `   `
- **Пустая строка:** ``

## Steps to reproduce
1. Залогиниться как `standard_user`
2. Добавить товар в корзину
3. Перейти к Checkout
4. Ввести First Name: `111`, Last Name: `111`
5. Нажать Continue → Finish

## Expected result
Ошибка валидации: «Имя должно содержать только буквы»

## Actual result
Заказ успешно оформлен

## Note
Баг воспроизводится как с пустой корзиной, так и с товарами.

## Attachments
- [Скриншот](../screenshots/screenshot-bug-004-name-validation.png)
