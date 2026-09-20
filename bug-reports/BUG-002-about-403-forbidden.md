# BUG-002: About возвращает 403 Forbidden

**Severity:** Minor
**Priority:** Low
**User:** standard_user
**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При нажатии на пункт **About** в гамбургер-меню открывается страница с ошибкой **403 Forbidden** (`saucelabs.com/403`).

## Steps to reproduce
1. Залогиниться как `standard_user`
2. Открыть гамбургер-меню (иконка ☰)
3. Нажать **About**

## Expected result
Открывается страница с информацией о SauceDemo

## Actual result
Открывается страница `saucelabs.com/403` с ошибкой **403 Forbidden**

## Attachments
- [Скриншот](../screenshots/screenshot-bug-002-about-403.png)
