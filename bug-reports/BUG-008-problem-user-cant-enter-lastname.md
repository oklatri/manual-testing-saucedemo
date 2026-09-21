# BUG-008: problem_user не может ввести Last Name, текст попадает в First Name

**Severity:** Major

**Priority:** High

**User:** problem_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При оформлении заказа под `problem_user` поле **Last Name не принимает ввод**. Буквы, которые пользователь печатает в поле Last Name, **попадают в поле First Name**, а Last Name остаётся пустым. Появляется ошибка «Error: Last Name is required».

## Steps to reproduce
1. Залогиниться как `problem_user` / `secret_sauce`
2. Добавить товар в корзину
3. Перейти к Checkout
4. Кликнуть в поле **Last Name**
5. Начать печатать (например, `Ivanov`)

## Expected result
Текст вводится в поле **Last Name**

## Actual result
Текст попадает в поле **First Name**, Last Name остаётся пустым

## Attachments
- [Скриншот](../screenshots/screenshot-bug-008-problem-user-lastname.png)

## Note
Это **известное поведение** демо-аккаунта `problem_user`. SauceDemo **специально** имитирует ошибки формы. Не является **реальным** дефектом.
