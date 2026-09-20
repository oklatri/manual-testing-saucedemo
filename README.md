# Manual Testing — SauceDemo

Портфолио ручного тестирования учебного сайта [SauceDemo](https://www.saucedemo.com/).

## Что это
SauceDemo — учебный интернет-магазин, созданный для практики тестирования. В нём 6 тестовых аккаунтов, каждый имитирует разное поведение.

## Инструменты
- Браузер (Chrome)
- DevTools
- Скриншоты

## Что внутри
- `test-cases.md` — тест-кейсы (логин, корзина, оформление заказа)
- `checklists.md` — чек-лист по аккаунтам
- `bug-reports/` — 12 баг-репортов
- `screenshots/` — скриншоты

## Тестовые аккаунты
| Логин | Пароль | Что имитирует |
|---|---|---|
| `standard_user` | `secret_sauce` | Обычный пользователь |
| `locked_out_user` | `secret_sauce` | Заблокированный |
| `problem_user` | `secret_sauce` | С багами UI |
| `performance_glitch_user` | `secret_sauce` | Медленный |
| `error_user` | `secret_sauce` | С ошибками формы |
| `visual_user` | `secret_sauce` | С визуальными багами |

## Покрытие
- Логин всех 6 аккаунтов
- Просмотр товаров
- Сортировка и фильтры
- Корзина (добавление, удаление)
- Оформление заказа
- Валидация формы

## Результаты
- 6 тест-кейсов
- 12 баг-репортов

## Найденные баги
- [BUG-001: Dynamic Catalog — бесконечная загрузка](bug-reports/BUG-001-dynamic-catalog-infinite-load.md)
- [BUG-002: About — 403 Forbidden](bug-reports/BUG-002-about-403-forbidden.md)
- [BUG-003: Reset App State — кнопки не обновляются](bug-reports/BUG-003-remove-button-not-updating.md)
- [BUG-004: Форма не валидирует имя](bug-reports/BUG-004-form-no-validation.md)
- [BUG-005: Заказ с пустой корзиной](bug-reports/BUG-005-order-with-empty-cart.md)
- [BUG-006: error_user — не вводится Last Name](bug-reports/BUG-006-error-user-cant-enter-lastname.md)
- [BUG-007: problem_user — одинаковые фото](bug-reports/BUG-007-problem-user-all-photos-same.md)
- [BUG-008: problem_user — не вводится Last Name](bug-reports/BUG-008-problem-user-cant-enter-lastname.md)
- [BUG-009: performance_glitch_user — медленная загрузка](bug-reports/BUG-009-performance-glitch-slow-loading.md)
- [BUG-010: visual_user — цены меняются](bug-reports/BUG-010-visual-user-changing-prices.md)
- [BUG-011: visual_user — значок корзины смещён](bug-reports/BUG-011-visual-user-cart-icon-misaligned.md)
- [BUG-012: visual_user — кнопка Continue смещена](bug-reports/BUG-012-visual-user-continue-button-misaligned.md)
