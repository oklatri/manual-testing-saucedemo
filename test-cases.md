# Test Cases — SauceDemo

## TC-001: Логин standard_user

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login

**Expected result:** Открывается страница с товарами

**Actual result:** Открывается страница с товарами

**Status:** ✅ Passed

---

## TC-002: Логин locked_out_user

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `locked_out_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login

**Expected result:** Ошибка «Sorry, this user has been locked out»

**Actual result:** Ошибка «Sorry, this user has been locked out»

**Status:** ✅ Passed

---

## TC-003: Логин problem_user

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `problem_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login

**Expected result:** Открывается страница с товарами

**Actual result:** Открывается страница с товарами, но все фото одинаковые (баг)

**Status:** ⚠️ Passed with issues (см. BUG-007)

---

## TC-004: Логин performance_glitch_user

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `performance_glitch_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login

**Expected result:** Страница грузится за 1–2 секунды

**Actual result:** Страница грузится 10+ секунд (баг)

**Status:** ⚠️ Passed with issues (см. BUG-009)

---

## TC-005: Логин error_user

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `error_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login

**Expected result:** Открывается страница с товарами

**Actual result:** Открывается страница с товарами

**Status:** ✅ Passed

---

## TC-006: Логин visual_user

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `visual_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login

**Expected result:** Открывается страница с товарами

**Actual result:** Открывается страница с товарами, но цены меняются (баг)

**Status:** ⚠️ Passed with issues (см. BUG-010)

---

## TC-007: Добавление товара в корзину

**Preconditions:** Открыт saucedemo.com, залогинен как `standard_user`
**Test data:** Sauce Labs Backpack

**Steps:**
1. Нажать **Add to cart** у товара Sauce Labs Backpack
2. Посмотреть на иконку корзины в правом верхнем углу

**Expected result:**
- Кнопка меняется на **Remove**
- Счётчик корзины показывает **1**

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-008: Удаление товара из корзины

**Preconditions:** Открыт saucedemo.com, залогинен, 1 товар в корзине

**Steps:**
1. Нажать **Remove** у товара
2. Посмотреть на счётчик корзины

**Expected result:**
- Кнопка меняется на **Add to cart**
- Счётчик корзины становится **пустым** (или 0)

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-009: Счётчик корзины обновляется при добавлении нескольких товаров

**Preconditions:** Открыт saucedemo.com, залогинен

**Steps:**
1. Добавить 3 разных товара в корзину
2. Посмотреть на счётчик

**Expected result:** Счётчик показывает **3**

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-010: Сортировка товаров по цене (low → high)

**Preconditions:** Открыт saucedemo.com, залогинен

**Steps:**
1. Открыть выпадающий список сортировки
2. Выбрать **Price (low to high)**

**Expected result:** Товары отсортированы по возрастанию цены

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-011: Сортировка товаров по имени (Z → A)

**Preconditions:** Открыт saucedemo.com, залогинен

**Steps:**
1. Открыть выпадающий список сортировки
2. Выбрать **Name (Z to A)**

**Expected result:** Товары отсортированы по убыванию имени

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-012: Checkout с пустой корзиной (негативный)

**Preconditions:** Открыт saucedemo.com, залогинен, корзина пуста

**Steps:**
1. Перейти в корзину
2. Нажать **Checkout**

**Expected result:** Кнопка Checkout **неактивна** или появляется ошибка «Корзина пуста»

**Actual result:** Переход на форму оформления заказа выполняется (см. BUG-005)
**Status:** ❌ Failed

---

## TC-013: Checkout с товаром — успешный заказ

**Preconditions:** Открыт saucedemo.com, залогинен, 1 товар в корзине

**Steps:**
1. Перейти в корзину
2. Нажать **Checkout**
3. Ввести First Name: `Ivan`, Last Name: `Petrov`, Zip: `123456`
4. Нажать **Continue**
5. Нажать **Finish**

**Expected result:**
- Открывается страница «Checkout: Complete!»
- Текст «Thank you for your order!»

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-014: Валидация First Name (пустое поле)

**Preconditions:** Открыт saucedemo.com, залогинен, 1 товар в корзине

**Steps:**
1. Перейти в корзину
2. Нажать **Checkout**
3. Оставить First Name пустым
4. Нажать **Continue**

**Expected result:** Ошибка «Error: First Name is required»

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed

---

## TC-015: Logout

**Preconditions:** Открыт saucedemo.com, залогинен

**Steps:**
1. Открыть гамбургер-меню (☰)
2. Нажать **Logout**

**Expected result:** Возврат на страницу логина

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed
