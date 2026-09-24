# Manual Testing — SauceDemo

Портфолио ручного тестирования учебного сайта [SauceDemo](https://www.saucedemo.com/).

## Что это
SauceDemo — учебный интернет-магазин, созданный для практики тестирования. В нём 6 тестовых аккаунтов, каждый имитирует разное поведение.

## Инструменты
- Браузер (Yandex Browser 150)
- DevTools
- Скриншоты

## Что внутри
- `test-cases.md` — тест-кейсы (логин, корзина, оформление заказа)
- `checklists.md` — чек-лист по аккаунтам
- `bug-reports/` — 12 баг-репортов
- `screenshots/` — скриншоты
- `test-plan.md` — тест-план проекта
- `jira-workflow.md` — процесс работы с багами (имитация Jira)
- `test-design.md` — техники тест-дизайна (EP, BVA, Decision Table, State Transition, Error Guessing, Decomposition)

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

## 🔗 Связь ручных тест-кейсов с автотестами

Часть ручных тест-кейсов автоматизирована в отдельном репозитории
[ui-automation-playwright](https://github.com/oklatri/ui-automation-playwright)
(Playwright + JavaScript + POM + GitHub Actions).

| Manual TC | Название | Автотест (Playwright) | Статус |
|---|---|---|---|
| TC-001 | Логин standard_user | `login.spec.js` → `TC-001: Login with standard_user` | ✅ automated |
| TC-002 | Логин locked_out_user | `login.spec.js` → `TC-002: Login with locked_out_user` | ✅ automated |
| TC-003 | Логин problem_user | — | ⚠️ manual only |
| TC-004 | Логин performance_glitch_user | — | ⚠️ manual only |
| TC-005 | Логин error_user | — | ⚠️ manual only |
| TC-006 | Логин visual_user | — | ⚠️ manual only |
| TC-007 | Добавление товара в корзину | `cart.spec.js` → `TC-007: Add one item to cart` | ✅ automated |
| TC-008 | Удаление товара из корзины | `cart.spec.js` → `TC-008: Remove item from cart` | ✅ automated |
| TC-009 | Счётчик корзины (3 товара) | `cart.spec.js` → `TC-009: Add multiple items to cart` | ✅ automated |
| TC-010 | Сортировка по цене (low → high) | — | ⚠️ manual only |
| TC-011 | Сортировка по имени (Z → A) | — | ⚠️ manual only |
| TC-012 | Checkout с пустой корзиной | — | ⚠️ manual only |
| TC-013 | Checkout с товаром — успешный заказ | — | ⚠️ manual only |
| TC-014 | Валидация First Name (пустое) | — | ⚠️ manual only |
| TC-015 | Logout | — | ⚠️ manual only |
| TC-016 | Корзина отображает добавленные товары | `cart.spec.js` → `TC-016: Cart shows added items` | ✅ automated |
| TC-017 | Логин с невалидными данными | `login.spec.js` → `TC-017: Login with invalid credentials` | ✅ automated |
| TC-018 | Логин с пустыми полями | `login.spec.js` → `TC-018: Login with empty fields` | ✅ automated |

**Итого:** 8 из 18 TC покрыты автотестами (44%), остальные 10 — только ручные.

### 📌 Кандидаты на автоматизацию (следующая итерация)
- TC-010, TC-011 — сортировка (стабильные, высокая ценность)
- TC-012 — негативный checkout (важный кейс)
- TC-013, TC-014 — позитивный checkout и валидация формы (ядро бизнес-логики)
- TC-015 — logout (простой, быстрый)

## Результаты
- 18 тест-кейсов
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
