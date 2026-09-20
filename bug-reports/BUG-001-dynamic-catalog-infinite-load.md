# BUG-001: Dynamic Catalog грузит бесконечно повторяющиеся товары

**Severity:** Minor
**Priority:** Low
**User:** standard_user
**Environment:** Chrome 120, Windows 11, saucedemo.com
**Related test case:** —

## Description
При открытии пункта **Dynamic Catalog** в гамбургер-меню страница **бесконечно подгружает** одни и те же товары. Список не заканчивается, товары повторяются.

## Steps to reproduce
1. Залогиниться как `standard_user`
2. Открыть гамбургер-меню (иконка ☰)
3. Нажать **Dynamic Catalog**
4. Прокрутить страницу вниз

## Expected result
Ограниченный список товаров (как на главной странице)

## Actual result
Бесконечная загрузка повторяющихся товаров

## Attachments
- [Скриншот](../screenshots/screenshot-bug-001-dynamic-catalog.png)
