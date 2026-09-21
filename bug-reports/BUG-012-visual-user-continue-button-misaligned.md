# BUG-012: visual_user — кнопка Continue смещена на странице Checkout

**Severity:** Minor

**Priority:** Low

**User:** visual_user

**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
При логине под `visual_user` на странице **Checkout: Your Information** кнопка **Continue** смещена от своего обычного положения — визуально не совпадает с расположением у `standard_user`.

## Steps to reproduce
1. Залогиниться как `visual_user` / `secret_sauce`
2. Добавить товар в корзину
3. Перейти к Checkout
4. Посмотреть на кнопку **Continue**

## Expected result
Кнопка Continue — на своём обычном месте

## Actual result
Кнопка Continue смещена

## Attachments
- [Скриншот](../screenshots/screenshot-bug-012-continue-button.png)

## Note
Это **известное поведение** демо-аккаунта `visual_user`. SauceDemo **специально** имитирует визуальные баги. Не является **реальным** дефектом.
