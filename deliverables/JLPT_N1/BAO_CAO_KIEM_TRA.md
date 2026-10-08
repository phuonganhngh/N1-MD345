# Báo cáo biên soạn và kiểm tra JLPT N1

Đã xuất **30 PDF**, chia đúng **10 nhóm**, tổng **276 trang A4 portrait**. Dùng 31 bộ script nguồn; 2 PDF cập nhật được dùng bổ sung lựa chọn in cho T12-2020 và T12-2022. Không thêm kỳ thi không có nguồn.

## Phạm vi thực tế

- 問題3: 176 câu; từng bộ có 5 hoặc 6 câu. Đáp án của cả bộ đứng trước script; không đưa phần hỏi/lựa chọn vào tài liệu 問題3.
- 問題4: 400 câu; từng bộ có 11, 13 hoặc 14 câu. Mỗi block gồm tình huống và duy nhất phản hồi đúng từ nguồn.
- 問題5: 82 phần script, tương ứng 113 câu hỏi khi tính riêng hai câu phụ ở phần cuối. Giai đoạn 2010–2019 có 3 phần; từ T12-2020 có 2 phần. Không ép mọi bộ thành cùng cấu trúc.

## Những chỗ cần bổ sung dữ liệu

**26 câu phụ thuộc 13 bộ** chưa đủ bằng chứng trực tiếp về thứ tự lựa chọn 1–4. Trang câu hỏi giữ câu hỏi gốc và ghi rõ cần bổ sung; không tự gắn số theo thứ tự xuất hiện trong hội thoại. Đáp án nguồn, script và bảng tóm tắt vẫn được giữ. Bảng so sánh ở các phần này dùng tên phương án và đánh dấu chưa xác minh số.

| Bộ | Câu cần bổ sung lựa chọn có số |
|---|---|
| T7-2010 | Q3.1, Q3.2 |
| T12-2011 | Q3.1, Q3.2 |
| T12-2012 | Q3.1, Q3.2 |
| T12-2015 | Q3.1, Q3.2 |
| T12-2016 | Q3.1, Q3.2 |
| T7-2017 | Q3.1, Q3.2 |
| T7-2018 | Q3.1, Q3.2 |
| T12-2018 | Q3.1, Q3.2 |
| T12-2019 | Q3.1, Q3.2 |
| T7-2021 | Q2.1, Q2.2 |
| T7-2023 | Q2.1, Q2.2 |
| T12-2023 | Q2.1, Q2.2 |
| T12-2024 | Q2.1, Q2.2 |

Ở T12-2017, 問題5 Q3.2: hội thoại nói người nữ dùng hai phiếu cho giải 2 và 3; khóa đáp án nguồn ghi 3. Bản biên soạn giữ nguyên khóa nguồn 3 và nội dung hội thoại, không tự đổi đáp án. Nên đối chiếu thêm đề/khóa chính thức nếu cần giải quyết điểm này.

## Kiểm tra cuối cùng

- Mở lại và render đủ 276 trang sau khi lưu. Không còn cảnh báo tài nguyên MuPDF.
- Đối chiếu hình ảnh 4618 crop với vùng nguồn tương ứng, có dung sai raster hóa; không còn crop bị đưa vào danh sách cần xem lại.
- 93 lượt kiểm tra bộ × Mondai: đủ nhãn câu, đúng thứ tự, đúng số đáp án theo mapping đã xác minh. Mỗi bộ bắt đầu ở trang mới.
- 問題4: tình huống và đáp án của từng câu nằm cùng một trang.
- 問題5: câu hỏi đứng riêng; trang sau bắt đầu bằng đáp án số, rồi script và bảng. Không có heading Answer trên phần này.
- Kiểm tra A4, rotation 0, lề ngang 43 pt ≈ 15,17 mm, tỷ lệ đồng nhất theo hai chiều. Crop dùng scale 0,93, không kéo giãn.
- Không còn pixel đỏ trong phần câu hỏi/lựa chọn 問題5 sau render. Script và trích dẫn dùng bản nguồn nguyên màu.
- SHA-256 của cả 33 PDF nguồn không đổi.

## Cách giữ nội dung gốc

Nội dung Nhật được copy bằng Form XObject từ vùng PDF nguồn. Giữ nguyên vector, text/font nếu nguồn có; đối với nguồn dùng image/mask, giữ nguyên tài nguyên ảnh/mask. Không OCR toàn PDF và không gõ lại nội dung Nhật. Text layer chỉ dùng cho vị trí. OCR chỉ áp dụng cho một số dòng nhỏ để tìm boundary của keyword lựa chọn; crop cuối cùng vẫn lấy từ PDF gốc và đã xem lại trực quan. Nhật trong bảng cũng là crop gốc. Tiếng Việt trong bảng là phần tóm tắt bổ sung.

Lưu PDF bằng chế độ giữ riêng stream tài nguyên, tránh lỗi mất mask/ảnh ở bước gộp tài nguyên trùng lặp. Hai file từng có cảnh báo đã được dựng lại và toàn bộ tài liệu đã được render, đối chiếu lại.

## Số câu từng bộ

| Bộ | 問題3 | 問題4 | 問題5 phần | 問題5 câu hỏi kể cả câu phụ |
|---|---:|---:|---:|---:|
| T7-2010 | 6 | 14 | 3 | 4 |
| T12-2010 | 5 | 14 | 3 | 4 |
| T7-2011 | 6 | 13 | 3 | 4 |
| T12-2011 | 6 | 13 | 3 | 4 |
| T7-2012 | 6 | 13 | 3 | 4 |
| T12-2012 | 5 | 14 | 3 | 4 |
| T7-2013 | 6 | 14 | 3 | 4 |
| T12-2013 | 5 | 14 | 3 | 4 |
| T7-2014 | 6 | 14 | 3 | 4 |
| T12-2014 | 6 | 14 | 3 | 4 |
| T7-2015 | 6 | 14 | 3 | 4 |
| T12-2015 | 6 | 14 | 3 | 4 |
| T7-2016 | 6 | 14 | 3 | 4 |
| T12-2016 | 6 | 14 | 3 | 4 |
| T7-2017 | 6 | 13 | 3 | 4 |
| T12-2017 | 6 | 13 | 3 | 4 |
| T7-2018 | 6 | 13 | 3 | 4 |
| T12-2018 | 6 | 13 | 3 | 4 |
| T7-2019 | 6 | 13 | 3 | 4 |
| T12-2019 | 6 | 13 | 3 | 4 |
| T12-2020 | 6 | 13 | 2 | 3 |
| T7-2021 | 6 | 13 | 2 | 3 |
| T12-2021 | 6 | 13 | 2 | 3 |
| T7-2022 | 6 | 13 | 2 | 3 |
| T12-2022 | 5 | 11 | 2 | 3 |
| T7-2023 | 5 | 11 | 2 | 3 |
| T12-2023 | 5 | 11 | 2 | 3 |
| T7-2024 | 5 | 11 | 2 | 3 |
| T12-2024 | 5 | 11 | 2 | 3 |
| T7-2025 | 5 | 11 | 2 | 3 |
| T12-2025 | 5 | 11 | 2 | 3 |

## Nhóm file và số trang

| Nhóm | Bộ | 問題3 | 問題4 | 問題5 |
|---|---|---:|---:|---:|
| 01 | T7-2010, T12-2010, T7-2011 | 6 | 6 | 13 |
| 02 | T12-2011, T7-2012, T12-2012 | 8 | 6 | 13 |
| 03 | T7-2013, T12-2013, T7-2014 | 8 | 6 | 16 |
| 04 | T12-2014, T7-2015, T12-2015 | 7 | 6 | 14 |
| 05 | T7-2016, T12-2016, T7-2017 | 7 | 6 | 17 |
| 06 | T12-2017, T7-2018, T12-2018 | 8 | 6 | 16 |
| 07 | T7-2019, T12-2019, T12-2020 | 9 | 6 | 15 |
| 08 | T7-2021, T12-2021, T7-2022 | 9 | 6 | 11 |
| 09 | T12-2022, T7-2023, T12-2023 | 6 | 6 | 9 |
| 10 | T7-2024, T12-2024, T7-2025, T12-2025 | 8 | 8 | 14 |

Mapping, thông số và kết quả kiểm tra máy nằm trong gói pipeline. README hướng dẫn chạy lại bằng các PDF nguồn, không cần OCR lại. Tổng số trang là kết quả dàn trang theo chiều cao crop, không phải chỉ tiêu cố định.
