# BUG-006: error_user не может ввести Last Name, но Continue активен

**Severity:** Major

**Priority:** High

**User:** error_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При оформлении заказа под `error_user` поле **Last Name не принимает ввод**. При этом кнопка **Continue остаётся активной**, и пользователь может перейти на следующий шаг. На шаге подтверждения кнопка **Finish не работает**.

## Steps to reproduce
1. Залогиниться как `error_user` / `secret_sauce`
2. Добавить товар в корзину
3. Перейти к Checkout
4. Ввести First Name (например, `Ivan`)
5. Попробовать ввести Last Name — **поле не принимает ввод**
6. Нажать Continue — переход работает
7. Нажать Finish — **кнопка не работает**

## Expected result
- Ошибка валидации: «Last Name is required»
- Кнопка Continue **заблокирована**, пока поле пустое

## Actual result
- Continue активен, переход работает
- Finish не работает

## Attachments
- [Скриншот](../screenshots/screenshot-bug-006-error-user-lastname.png)

## Note
Это **известное поведение** демо-аккаунта `error_user`. SauceDemo **специально** имитирует ошибки формы для тестирования. Не является **реальным** дефектом.
