# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): Đinh Trường Phong        Người kiểm (học viên): Đinh Trường Phong (Tự kiểm tra / Self-QC)  
Ngày: 2026-11-20                                  Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): phong-front.zip, phong-fisheye.zip (revision 1)  
Số ảnh kiểm: 20 core (+ 8 ảnh thêm)               Số nhãn đã kiểm (shape + tag): 296  

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 28 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 20 | 0 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 41 | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 41 | 0 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 41 | 0 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 41 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 45 | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 23 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 32 | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 32 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 20 | 0 | chính |
| QC1-12 file | lỗi file | 2 | 0 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-02 | A05 | lane | miễn trừ | Mặt đường thực tế không có vạch sơn kẻ làn (chỉ có mép vỉa hè road_curb) |
| 2 | QC1-02 | A06 | lane (R1) | miễn trừ | Bên phải làn xe chạy sát mép lề, không có vạch sơn phân làn |
| 3 | QC1-02 | A09 | lane (R1) | miễn trừ | Bên phải làn xe chạy không có vạch kẻ sơn |
| 4 | QC1-02 | A10 | lane (R1) | miễn trừ | Bên phải là dải đỗ xe / lề đường, không có vạch sơn kẻ đường |
| 5 | QC1-02 | A14 | lane (R1) | miễn trừ | Ảnh đêm tối, vạch không nhìn rõ thì không vẽ thêm |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05 | Đường không có vạch sơn thì có cần vẽ L1/R1 không? | Không vẽ; ca này được miễn trừ QC1-02 theo quy định Checkpoint của lab |
| B03 | Vạch đứt ngắn gồm 3 vệt sơn thẳng có bắt buộc nhiều điểm không? | Đã bổ sung điểm để đảm bảo khớp quy định cung cong fisheye |

## Quyết định
Lỗi nặng: 0   Lỗi chính: 0 / 296 nhãn = 0.0 %   Lỗi nhẹ: 0   Ca chờ lead: 0  
Quyết định (Release / Hold / Rework): **Release**  
Lý do (theo luật của phiếu): Không còn lỗi nặng; tỉ lệ lỗi chính = 0% (< 5%); các trường hợp thiếu vạch L1/R1 đều thuộc ca thực tế không có vạch và được miễn trừ hợp lệ.  

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
