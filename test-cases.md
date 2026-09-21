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

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`
- Товар: Sauce Labs Backpack

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Нажать **Add to cart** у товара Sauce Labs Backpack
5. Посмотреть на иконку корзины

**Expected result:**
- Кнопка меняется на **Remove**
- Счётчик корзины показывает **1**

**Actual result:**
- Кнопка меняется на **Remove**
- Счётчик показывает **1**

**Status:** ✅ Passed

---

## TC-008: Удаление товара из корзины

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Добавить товар в корзину
5. Нажать **Remove** у товара
6. Посмотреть на счётчик корзины

**Expected result:**
- Кнопка меняется на **Add to cart**
- Счётчик корзины пустой

**Actual result:**
- Кнопка меняется на **Add to cart**
- Счётчик пустой

**Status:** ✅ Passed

---

## TC-009: Счётчик корзины обновляется при добавлении нескольких товаров

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`
- Товары: Backpack, Bike Light, T-Shirt

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Добавить 3 разных товара в корзину
5. Посмотреть на счётчик

**Expected result:** Счётчик показывает **3**

**Actual result:** Счётчик показывает **3**

**Status:** ✅ Passed

---

## TC-010: Сортировка товаров по цене (low → high)

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Открыть выпадающий список сортировки
5. Выбрать **Price (low to high)**

**Expected result:** Товары отсортированы по возрастанию цены

**Actual result:** Товары отсортированы по возрастанию цены

**Status:** ✅ Passed

---

## TC-011: Сортировка товаров по имени (Z → A)

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Открыть выпадающий список сортировки
5. Выбрать **Name (Z to A)**

**Expected result:** Товары отсортированы по убыванию имени

**Actual result:** Товары отсортированы по убыванию имени

**Status:** ✅ Passed

---

## TC-012: Checkout с пустой корзиной (негативный)

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Перейти в корзину (не добавляя товары)
5. Нажать **Checkout**

**Expected result:** Кнопка Checkout неактивна или ошибка «Корзина пуста»

**Actual result:** Переход на форму оформления выполняется (см. BUG-005)

**Status:** ❌ Failed

---

## TC-013: Checkout с товаром — успешный заказ

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`
- First Name: `Ivan`
- Last Name: `Petrov`
- Zip: `123456`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Добавить товар в корзину
5. Нажать **Checkout**
6. Ввести First Name, Last Name, Zip
7. Нажать **Continue**
8. Нажать **Finish**

**Expected result:** Открывается страница «Checkout: Complete!» с текстом «Thank you for your order!»

**Actual result:** Открывается страница «Checkout: Complete!»

**Status:** ✅ Passed

---

## TC-014: Валидация First Name (пустое поле)

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Добавить товар в корзину
5. Нажать **Checkout**
6. Оставить First Name пустым
7. Нажать **Continue**

**Expected result:** Ошибка «Error: First Name is required»

**Actual result:** Ошибка «Error: First Name is required»

**Status:** ✅ Passed

---

## TC-015: Logout

**Preconditions:** Открыт saucedemo.com

**Test data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Ввести username
2. Ввести password
3. Нажать Login
4. Открыть гамбургер-меню (☰)
5. Нажать **Logout**

**Expected result:** Возврат на страницу логина

**Actual result:** Возврат на страницу логина

**Status:** ✅ Passed

**Actual result:** Совпадает с ожидаемым
**Status:** ✅ Passed
