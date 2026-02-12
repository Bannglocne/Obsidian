## I. Các Khái Niệm Nền Tảng về Máy Ảnh và Phơi Sáng
### The Exposure Triangle
Phơi sáng là lượng ánh sáng được ghi nhận bởi cảm biến hình ảnh, được quyết định bởi ba yếu tố cốt lõi: khẩu độ, tốc độ màn trập và độ nhạy ISO. Sự kết hợp hài hòa giữa ba yếu tố này quyết định độ sáng tối và các hiệu ứng nghệ thuật của bức ảnh.

| Yếu Tố                              | Chức Năng Chính                                      | Tác Động Phụ                                      | Mô Tả Chi Tiết                                                                                                                                                                                                                                                                                  |
| ----------------------------------- | ---------------------------------------------------- | ------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Khẩu Độ (Aperture)**              | Điều khiển lượng ánh sáng đi qua ống kính.           | Kiểm soát **Độ Sâu Trường Ảnh (DOF)**.            | Được đo bằng chỉ số f (f-stop).<br>**Chỉ số f càng nhỏ** (ví dụ f/1.8), khẩu độ càng mở lớn, lượng sáng vào càng nhiều, và DOF càng mỏng (làm mờ hậu cảnh).<br>**Chỉ số f càng lớn** (ví dụ f/16), khẩu độ càng khép nhỏ, lượng sáng vào càng ít, và DOF càng dày (nhiều vùng của ảnh rõ nét).        |
| **Tốc Độ Màn Trập (Shutter Speed)** | Điều khiển thời gian cảm biến tiếp xúc với ánh sáng. | Kiểm soát sự thể hiện của **chuyển động**.        | Được đo bằng giây hoặc phần của giây.<br>**Tốc độ nhanh** (ví dụ 1/1000s) "đóng băng" chuyển động, bắt dính các đối tượng di chuyển nhanh.<br>**Tốc độ chậm** (ví dụ 1s) tạo ra hiệu ứng mờ nhòe (motion blur) cho các đối tượng chuyển động, thích hợp để chụp cảnh đêm hoặc dòng nước chảy mềm mại. |
| **Độ Nhạy Sáng (ISO)**              | Điều chỉnh độ nhạy của cảm biến với ánh sáng.        | Ảnh hưởng đến **độ nhiễu (noise) / hạt** của ảnh. | **ISO thấp** (ví dụ 100, 200) cho chất lượng ảnh mịn màng, ít nhiễu nhất, phù hợp với điều kiện đủ sáng.<br>**ISO cao** (ví dụ 800, 1600) cho phép chụp trong điều kiện thiếu sáng mà không cần flash hoặc chân máy, nhưng ảnh sẽ bị nhiễu và vỡ hạt nhiều hơn.                                    |

### Exposure Compensation & Metering
Mọi máy ảnh đều được tích hợp một chip đo sáng để tự động quyết định các thông số phơi sáng. Tuy nhiên, cơ chế này hoạt động dựa trên nguyên tắc tính toán để đưa toàn bộ khung cảnh về một mức xám trung tính 18%. Điều này dẫn đến sai sót trong các tình huống đặc biệt (Quá sáng / Quá tối)

=> Lúc này, nhiếp ảnh gia cần sử dụng chức năng **Bù trừ sáng (Exposure Compensation - EV)** để "ra lệnh" cho máy ảnh điều chỉnh lại độ sáng cho đúng ý đồ.
- **+EV:** Làm ảnh sáng hơn. Dùng cho các chủ thể sáng màu hoặc khi chụp ngược sáng.
- **-EV:** Làm ảnh tối hơn. Dùng cho các chủ thể tối màu để giữ được màu đen sâu.

**Các trường hợp bù sáng cơ bản:**
- Cảnh quá sáng, nắng rực rỡ: +1 EV đến +3 EV
- Cảnh bãi biển, mặt sông phản sáng: +0.7 EV đến +3 EV
- Cận cảnh vật thể sáng màu (hoa vàng): +1 EV đến +1.7 EV
- Phong cảnh nhiều bóng râm: -0.5 EV
- Vật thể tối màu (nhà cổ, tường xám): -1.5 EV đến +0.5 EV

Để đưa ra quyết định phơi sáng, máy ảnh sử dụng các **chế độ đo sáng** khác nhau:
1. **Đo sáng toàn cảnh (Evaluative/Matrix Metering):** Chế độ mặc định, máy đo sáng trên toàn bộ khung hình và tính toán để đưa ra kết quả tối ưu. Phù hợp với hầu hết các tình huống thông thường.
2. **Đo sáng trung tâm (Center-weighted Metering):** Ưu tiên đo sáng vào vùng trung tâm của khung hình, ít quan tâm đến các vùng rìa. Hữu ích khi chủ thể chính nằm ở giữa.
3. **Đo sáng điểm/một phần (Spot/Partial Metering):** Chỉ đo sáng tại một vùng rất nhỏ ở trung tâm (hoặc liên kết với điểm lấy nét). Rất hiệu quả khi có sự chênh lệch sáng tối lớn giữa chủ thể và hậu cảnh (ví dụ chụp ngược sáng).

### Exposure Testing Tools
- **Biểu đồ Histogram:** Là một biểu đồ thể hiện sự phân bổ các vùng sáng tối trong ảnh. Trục ngang biểu diễn độ sáng từ đen tuyền (bên trái) đến trắng tinh (bên phải). Nếu biểu đồ lệch hẳn về bên trái, ảnh bị thiếu sáng. Nếu lệch hẳn về bên phải, ảnh bị dư sáng. Một biểu đồ cân đối, có dạng hình quả đồi ở giữa, cho thấy ảnh được phơi sáng tốt.
- **Cảnh báo vùng cháy sáng (Highlight Warning):** Một tính năng trên màn hình LCD, các vùng ảnh bị dư sáng quá mức (mất hoàn toàn chi tiết) sẽ nhấp nháy. Đây là công cụ hữu ích để kiểm tra và điều chỉnh lại phơi sáng ngay lập tức.
- **Chụp bù trừ sáng tự động (Auto Exposure Bracketing - AEB):** Chế độ này cho phép máy tự động chụp liên tiếp 3 hoặc 5 tấm ảnh với các mức phơi sáng khác nhau (ví dụ: -1 EV, 0 EV, +1 EV). Đây là một giải pháp an toàn khi không chắc chắn về điều kiện ánh sáng.

## II. Bố Cục và Ngôn Ngữ Hình Ảnh
### Các Quy Tắc Bố Cục Kinh Điển

1. **Quy tắc 1/3:** Tưởng tượng khung hình được chia làm 9 phần bằng nhau bởi hai đường ngang và hai đường dọc. Thay vì đặt chủ thể chính vào giữa, hãy đặt nó vào các giao điểm hoặc dọc theo các đường kẻ này. Hầu hết các máy ảnh compact và DSLR đều có tính năng hiển thị lưới (Frame assist) để hỗ trợ quy tắc này.
2. **Đường Chân Trời:** Không bao giờ đặt đường chân trời cắt ngang chính giữa bức ảnh. Hãy đặt nó ở đường 1/3 phía trên (để nhấn mạnh tiền cảnh) hoặc 1/3 phía dưới (để nhấn mạnh bầu trời).
3. **Đường Dẫn (Leading Lines):** Sử dụng các đường nét tự nhiên trong cảnh (con đường, dòng sông, hàng rào) để dẫn mắt người xem đi vào bên trong ảnh, hướng tới chủ thể chính. Các đường cong hình chữ "S" hoặc chữ "C" tạo cảm giác mềm mại và chậm rãi, hấp dẫn hơn đường thẳng.
4. **Điểm Mạnh Duy Nhất:** Mỗi bức ảnh chỉ nên có một điểm mạnh, một chủ đề chính duy nhất để tránh làm người xem phân tâm.
5. **Sử Dụng Khung Tự Nhiên:** Tận dụng các yếu tố trong cảnh như ô cửa, vòm cây, cổng chào để tạo thành một "khung trong khung", giúp tập trung sự chú ý vào chủ thể và tăng chiều sâu cho ảnh.

###  Lấy Nét và Độ Sâu Trường Ảnh
- **Độ Sâu Trường Ảnh (Depth of Field - DOF):** Là vùng không gian phía trước và sau điểm lấy nét mà các vật thể trong đó vẫn hiện ra rõ nét. DOF được kiểm soát chủ yếu bằng khẩu độ:
    - **Khẩu độ lớn (chỉ số f nhỏ):** DOF mỏng, chỉ có chủ thể nét, tiền cảnh và hậu cảnh bị xóa mờ.
    - **Khẩu độ nhỏ (chỉ số f lớn):** DOF dày, nhiều vùng trong ảnh từ gần đến xa đều rõ nét.
- **Các loại nhòe (Blur):**
    - **Out of Focus (Mất nét):** Xảy ra khi máy ảnh không lấy nét đúng vào chủ thể.
    - **Motion Blur (Nhòe do chuyển động):** Xảy ra khi chủ thể di chuyển trong lúc màn trập đang mở hoặc máy ảnh bị rung (camera shake).
- **Lấy nét tự động (Autofocus - AF):** Máy ảnh DSLR được thiết kế để lấy nét rất nhanh. Cần chọn đúng chế độ lấy nét: AF-S (Single) cho chủ thể đứng yên và AF-C (Continuous) cho chủ thể đang di chuyển.

## III. Quản Lý Màu Sắc và Định Dạng Tệp
### White Balance - WB
Các nguồn sáng khác nhau (mặt trời, bóng râm, đèn điện) có "nhiệt độ màu" khác nhau, gây ra hiện tượng ám màu trên ảnh. Chức năng Cân bằng trắng giúp khử các ám màu này, trả lại màu trắng đúng với thực tế, từ đó các màu khác cũng sẽ được tái hiện chính xác.
- **Auto WB (AWB):** Máy tự động điều chỉnh, hiệu quả trong hầu hết các trường hợp.
- **Các chế độ cài đặt sẵn:** Daylight (Ánh sáng ban ngày), Cloudy (Trời nhiều mây), Shade (Bóng râm), Tungsten (Đèn dây tóc), Fluorescent (Đèn huỳnh quang), Flash.

### Picture Styles và Tùy Chỉnh Màu Sắc
Đây là các chế độ cài đặt sẵn trong máy ảnh (đặc biệt của Canon) giúp người dùng lựa chọn phong cách màu sắc và hình ảnh mong muốn mà không cần xử lý hậu kỳ. Mỗi Picture Style là một sự kết hợp của 4 thông số cơ bản:
1. **Độ nét (Sharpness):** Độ sắc nét của các đường viền.
2. **Độ tương phản (Contrast):** Sự khác biệt giữa vùng sáng và vùng tối.
3. **Độ bão hòa màu (Saturation):** Cường độ, độ rực rỡ của màu sắc.
4. **Tông màu (Hue/Color Tone):** Nền màu chung của bức ảnh.

**Các Picture Style tiêu chuẩn:**
- **Standard (Tiêu chuẩn):** Cho ảnh sắc nét, màu sắc sinh động, phù hợp với đa số tình huống.
- **Portrait (Chân dung):** Làm cho màu da trở nên mềm mại, tươi sáng.
- **Landscape (Phong cảnh):** Tăng cường độ rực rỡ cho màu xanh lá, xanh dương và vàng.
- **Neutral (Trung tính):** Giảm nhẹ màu sắc và độ nét, phù hợp để xử lý hậu kỳ.
- **Faithful (Chân thực):** Tái tạo màu sắc gần với thực tế nhất dưới ánh sáng chuẩn 5200K.
- **Monochrome (Đơn sắc):** Chuyển ảnh sang dạng đen trắng.
