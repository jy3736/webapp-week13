## 把『函數』傳遞給另一函數當作`參數`，用來過濾陣列中的資料。

- 把『函數』用作參數在 JavaScript 是非常常見的應用技巧。
- 請參考 `apply(...)` 與 `gt10(...)` 的使用方式，另外撰寫兩個過濾函數：
    - `even(v)` 如果 `v` 是偶數則回傳『真』。
    - `odd(v)` 如果 `v` 是奇數則回傳『真』。

### 在 Windows 簡易測試
```shell
lab04> 1..30 | Get-Random -Count 20 | node .\main.js
gt10(v) => 27,19,12,29,18,26,14,17,28,13,21,15,23,30
even(v) => 6,8,4,12,18,26,14,28,10,30
odd(v)  => 7,27,19,29,17,3,13,21,15,23

lab04> 1..30 | Get-Random -Count 20 | node .\main.js
gt10(v) => 22,19,12,28,17,26,16,30,24,29,14,25
even(v) => 22,4,12,28,26,8,16,30,24,10,14
odd(v)  => 19,17,9,7,5,3,29,25,1
```

### 在 Windows 使用自動批閱測試 (修改完程式後的測試)
```shell
lab04> .\test.ps1
Test Data : 1 4 14 13 8 11 4 24 26 26 27 16 19
Test Data : 12 13 23 17 14 3 2 6 18 5 6 3 25 28 30 26 27 13
Test Data : 8 14 7 17 7 10 13 20 2 13 9 5 30 3 19 3 12 14 7
Test Data : 14 19 7 21 14 28 19 20 9 11 27 24 10 19 3 30
Test Data : 3 16 27 16 2 24 1 21 18 9 20 16 17 7 17 19 29 21 4 21 13 5 6 9 4
Test Data : 14 29 20 17 20 17 29 14 3 30 25
Test Data : 10 5 23 21 12 23 20 23 23 4 22 20 2 18 8 25 3 17 27 1 7 15 23 23 19
Test Data : 20 24 30 16 2 3 26 20 10 25 13 21 9 11 22 1 17 2 7 27 11
Test Data : 21 5 3 26 17 13 15 27 17 9 14 23 14 6 20 16 28 4 9
Test Data : 29 14 4 19 6 30 9 2 10 13 22 15 22 15 17 11 16 12 9 29 14 20 12 4 1 20 22

測試通過!

gt10(v) => 29,14,19,30,13,22,15,22,15,17,11,16,12,29,14,20,12,20,22
even(v) => 14,4,6,30,2,10,22,22,16,12,14,20,12,4,20,22
odd(v)  => 29,19,9,13,15,15,17,11,9,29,1
```
