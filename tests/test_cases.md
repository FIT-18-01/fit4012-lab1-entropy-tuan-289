# Test cases – FIT4012 Lab 1

Đánh dấu [x] khi đã chạy và kiểm tra kết quả.

## 1. Entropy / Redundancy
- [x] Input: `aaaa` -> entropy thấp, redundancy cao
- [x] Input: `abcd` -> entropy cao hơn `aaaa`
- [x] Input: `hello world` -> entropy và redundancy được tính hợp lệ
- [x] Input: `ABAABA` -> kiểm tra ký tự lặp không đều
- [x] Input: `` -> kiểm tra trường hợp chuỗi rỗng

## 2. Modulo inverse
- [x] `a=3, m=7` -> nghịch đảo modulo là 5
- [x] `a=10, m=17` -> nghịch đảo modulo là 12
- [x] `a=6, m=9` -> không tồn tại nghịch đảo modulo
- [x] `a=1, m=11` -> nghịch đảo modulo là 1
- [x] `a=14, m=15` -> nghịch đảo modulo là 14

## 3. Ghi chú
Thêm test riêng của nhóm nếu cần.
