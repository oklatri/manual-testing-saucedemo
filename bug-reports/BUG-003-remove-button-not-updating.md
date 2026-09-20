# BUG-003: Кнопка «Remove» не меняется на «Add to cart» после Reset App State и смены фильтров

**Severity:** Major
**Priority:** High
**User:** standard_user
**Environment:** Chrome 120, Windows 11, saucedemo.com

## Description
После добавления товара в корзину кнопка меняется на **«Remove»**. Если затем нажать **Reset App State** в гамбургер-меню или сменить **фильтр** (например, Price high to low) — товары пропадают из корзины, но кнопки **остаются «Remove»** вместо «Add to cart».

## Steps to reproduce

### Сценарий 1: Reset App State
1. Залогиниться как `standard_user`
2. Добавить товар в корзину (кнопка станет «Remove»)
3. Открыть гамбургер-меню
4. Нажать **Reset App State**

### Сценарий 2: Смена фильтра
1. Залогиниться как `standard_user`
2. Добавить товар в корзину (кнопка станет «Remove»)
3. Сменить фильтр (например, «Price (high to low)»)

## Expected result
Корзина пуста, кнопки — **«Add to cart»**

## Actual result
Корзина пуста, но кнопки — **«Remove»**

## Note
После перезагрузки страницы кнопки становятся «Add to cart».

## Attachments
- [Скриншот](../screenshots/screenshot-bug-003-remove-button.png)
