# BUG-005: Можно оформить заказ с пустой корзиной

**Severity:** Major

**Priority:** High
**User:** standard_user
**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
Система позволяет оформить заказ, когда корзина **пуста**. Приложение должно **блокировать** кнопку Checkout или показывать ошибку «Корзина пуста».

## Steps to reproduce
1. Залогиниться как `standard_user`
2. **Не добавлять** товары в корзину
3. Перейти в корзину (иконка корзины)
4. Нажать **Checkout**
5. Заполнить форму (First Name, Last Name, Zip)
6. Нажать **Continue**
7. Нажать **Finish**

## Expected result
Ошибка «Корзина пуста, добавьте товары»

## Actual result
Заказ успешно оформлен

## Attachments
- [Скриншот](../screenshots/screenshot-bug-005-empty-cart.png)
