# BUG-010: visual_user — цены меняются при каждом обновлении страницы

**Severity:** Major

**Priority:** High

**User:** visual_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При логине под `visual_user` **цены товаров меняются** при каждом обновлении страницы (F5). Например, Backpack: $63.26 → $31.35 → $85.28. Цены **не должны** меняться сами по себе.

## Steps to reproduce
1. Залогиниться как `visual_user` / `secret_sauce`
2. Записать цену Sauce Labs Backpack (например, $63.26)
3. Обновить страницу (F5)
4. Снова записать цену

## Expected result
Цена не меняется при обновлении

## Actual result
Цена каждый раз другая ($31.35, $85.28 и т.д.)

## Attachments
- [Скриншот](../screenshots/screenshot-bug-010-visual-user-prices-1.png)
- [Скриншот](../screenshots/screenshot-bug-010-visual-user-prices-2.png)
- [Скриншот](../screenshots/screenshot-bug-010-visual-user-prices-3.png)
