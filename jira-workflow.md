# Jira Workflow — SauceDemo

## Процесс работы с багами

1. **Баг** **найден** → **создать** **тикет** в **Jira**.
2. **Тикет** **проходит** **статусы**: `Open` → `In Progress` → `Ready for QA` → `Closed`.
3. **Тестировщик** **проверяет** **фикс** → **закрывает** **тикет**.

## Пример тикета

**ID:** BUG-001
**Summary:** Dynamic Catalog грузит бесконечно
**Type:** Bug
**Priority:** Low
**Status:** Open
**Reporter:** Сергей (QA)
**Assignee:** —
**Environment:** Chrome 120, Windows 11

**Description:**
При открытии Dynamic Catalog в гамбургер-меню страница бесконечно подгружает товары.

**Steps to Reproduce:**
1. Залогиниться как standard_user
2. Открыть гамбургер-меню
3. Нажать Dynamic Catalog

**Expected:** Ограниченный список товаров
**Actual:** Бесконечная загрузка

**Attachments:** screenshot-bug-001-dynamic-catalog.png
