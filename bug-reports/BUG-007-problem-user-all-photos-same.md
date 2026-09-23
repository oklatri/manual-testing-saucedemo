# BUG-007: problem_user — все товары имеют одинаковое фото

**Severity:** Minor

**Priority:** Medium

**User:** problem_user

**Environment:** Yandex Browser 150, Windows 10 22H2, saucedemo.com

## Description
При логине под `problem_user` **все товары** отображаются с **одним и тем же фото** — собака с мячиком. Хотя названия товаров разные (Backpack, Bike Light, T-Shirt и т.д.), картинки одинаковые.

## Steps to reproduce
1. Залогиниться как `problem_user` / `secret_sauce`
2. Посмотреть на страницу товаров
3. Сравнить фото у разных товаров

## Expected result
У каждого товара — **своё фото**

## Actual result
У всех товаров — **фото собаки с мячиком**

## Attachments
- [Скриншот](../screenshots/screenshot-bug-007-problem-user-photos.png)

## Note
Это **известное поведение** демо-аккаунта `problem_user`. SauceDemo **специально** показывает одинаковые фото для тестирования. Не является **реальным** дефектом.
