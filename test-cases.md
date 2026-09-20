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
