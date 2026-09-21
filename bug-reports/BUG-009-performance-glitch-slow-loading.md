# BUG-009: performance_glitch_user — медленная загрузка страниц

**Severity:** Major

**Priority:** Medium

**User:** performance_glitch_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При логине под `performance_glitch_user` страницы **грузятся значительно дольше обычного** — 10+ секунд вместо 1–2. Также наблюдается **высокая нагрузка на CPU** и подвисания браузера.

## Steps to reproduce
1. Залогиниться как `performance_glitch_user` / `secret_sauce`
2. Замерить время загрузки страницы товаров (DevTools → Network)
3. Сравнить с `standard_user`

## Expected result
Страница грузится за 1–2 секунды

## Actual result
Страница грузится 10+ секунд, высокая нагрузка на CPU

## Note
Это **известное поведение** демо-аккаунта `performance_glitch_user`. SauceDemo **специально** имитирует медленную загрузку. Не является **реальным** дефектом.
