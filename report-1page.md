# Report 1 Page – FIT4012 Lab 1

## 1. Mục tiêu
Bài lab yêu cầu đọc hiểu và xây dựng chương trình tính entropy của một chuỗi ký tự, bổ sung chức năng tính độ dư thừa thông tin, và cài đặt hàm tìm nghịch đảo modulo bằng thuật toán Euclid mở rộng.

## 2. Cách làm
- Đọc mã nguồn mẫu và hiểu cách tính tần suất xuất hiện ký tự.
- Viết hàm `calculate_redundancy()` theo công thức `R = log2(N) - H(X)` với `N = 256`.
- Hoàn thiện hàm `mod_inverse()` dùng hàm `extended_euclid()` để tìm nghịch đảo modulo.
- Thêm các test case trong `tests/test_cases.md` và ghi log thực thi.

## 3. Kết quả chính
### 3.1 Entropy và redundancy
| Input | Entropy | Redundancy | Nhận xét |
|---|---:|---:|---|
| `aaaa` | 0.0 | 8.0 | Chuỗi đồng nhất có entropy thấp nhất |
| `abcd` | 2.0 | 6.0 | 4 ký tự khác nhau tạo entropy cao hơn |
| `hello world` | 2.845 | 5.155 | Chuỗi có ký tự lặp và khoảng trắng |
| `ABAABA` | 1.459 | 6.541 | Phân phối ký tự không đồng đều |
| `` | 0.0 | 0.0 | Chuỗi rỗng xử lý an toàn |

### 3.2 Modulo inverse
| a | m | Kết quả mong đợi | Kết quả chương trình |
|---|---:|---|---|
| 3 | 7 | 5 | 5 |
| 10 | 17 | 12 | 12 |
| 6 | 9 | Không tồn tại | Không tồn tại |
| 1 | 11 | 1 | 1 |
| 14 | 15 | 14 | 14 |

## 4. Kết luận
Qua bài lab, em hiểu rõ hơn cách entropy đo lượng thông tin và độ dư thừa của chuỗi ký tự, đồng thời nắm cách dùng thuật toán Euclid mở rộng để tính nghịch đảo modulo. Khó khăn lớn nhất là đảm bảo xử lý các trường hợp biên như chuỗi rỗng và trường hợp không tồn tại nghịch đảo, nhưng điều này được giải quyết bằng kiểm tra gcd và xử lý giá trị trả về của hàm mở rộng.
