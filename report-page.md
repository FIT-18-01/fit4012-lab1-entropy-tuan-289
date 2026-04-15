# Report 1 Page – FIT4012 Lab 1

## 1. Mục tiêu
Bài lab yêu cầu đọc hiểu chương trình tính entropy, bổ sung tính độ dư thừa thông tin, và cài đặt nghịch đảo modulo bằng thuật toán Euclid mở rộng.

## 2. Cách làm
- Viết hàm `calculate_redundancy()` theo công thức `R = log2(N) - H(X)` với `N = 256`.
- Hoàn thiện hàm `mod_inverse()` dùng `extended_euclid()` để tìm nghịch đảo modulo.
- Thêm các test case và ghi log chạy thử.

## 3. Kết quả chính
### 3.1 Entropy và redundancy
| Input | Entropy | Redundancy | Nhận xét |
|---|---:|---:|---|
| `aaaa` | 0.0 | 8.0 | Chuỗi đồng nhất, entropy thấp |
| `abcd` | 2.0 | 6.0 | 4 ký tự khác nhau tạo entropy cao hơn |
| `hello world` | 2.845 | 5.155 | Chuỗi có ký tự lặp và khoảng trắng |
| `ABAABA` | 1.459 | 6.541 | Phân phối ký tự không đều |
| `` | 0.0 | 0.0 | Chuỗi rỗng xử lý an toàn |

### 3.2 Modulo inverse
| a | m | Kết quả mong đợi | Kết quả chương trình |
|---:|---:|---|---|
| 3 | 7 | 5 | 5 |
| 10 | 17 | 12 | 12 |
| 6 | 9 | Không tồn tại | Không tồn tại |
| 1 | 11 | 1 | 1 |
| 14 | 15 | 14 | 14 |

## 4. Kết luận
Qua bài lab, em đã hiểu rõ cách entropy đo lượng thông tin và cách tính độ dư thừa dựa trên entropy thực tế. Em cũng nắm được cách dùng thuật toán Euclid mở rộng để tìm nghịch đảo modulo và kiểm thử chương trình với nhiều trường hợp biên.
