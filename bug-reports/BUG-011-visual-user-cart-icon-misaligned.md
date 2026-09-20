# BUG-011: visual_user — значок корзины смещён

**Severity:** Minor

**Priority:** Low

**User:** visual_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При логине под `visual_user` **значок корзины** в правом верхнем углу **смещён** от своего обычного положения. Визуально не совпадает с расположением у `standard_user`.

## Steps to reproduce
1. Залогиниться как `visual_user` / `secret_sauce`
2. Посмотреть на значок корзины в правом верхнем углу
3. Сравнить с `standard_user`

## Expected result
Значок корзины — на своём обычном месте

## Actual result
Значок корзины смещён

## Attachments
- [Скриншот](../screenshots/screenshot-bug-011-cart-icon.png)
