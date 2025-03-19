# SOICT - Hệ nhúng

Học liệu dành cho học phần Hệ nhúng

## Mục lục

- [Tool Kit - Bộ công cụ thực hành STM32 và Arduino](#tool-kit---bộ-công-cụ-thực-hành-stm32-và-arduino)
- [Phần mềm STM32 CubeIDE](#phần-mềm-stm32-cubeide)
  - [Cài đặt phần mềm STM32 CubeIDE](#cài-đặt-phần-mềm-stm32-cubeide)
  - [Tạo dự án mới với STM32 CubeIDE](#tạo-dự-án-mới-với-stm32-cubeide)
- [Breadboard cắm dây](#breadboard-cắm-dây)
- [Các bài thực hành](#các-bài-thực-hành)
  1. [Nháy đèn buit-in LED trên board](#nháy-đèn-buit-in-led-trên-board)
  2. [Mở rộng - Nháy đèn LED lắp ngoài](#mở-rộng---nháy-đèn-led-lắp-ngoài)


## Tool Kit - Bộ công cụ thực hành STM32 và Arduino

**Toàn cảnh**\
![Hộp 1](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/cc05d098-bf48-4706-adfa-b92327892a7c)
**Mặt trước**\
![Hộp 2](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/a1124c69-0bef-46ca-b4bc-4a5ccf273e12)
**Bên trong**\
![Mở nắp](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/ad94bd1b-7fd9-438d-a766-9e467c00763d)

- Danh sách linh kiện\
  ![Danh sách linh kiện](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/c87d6015-2907-4a42-bd65-dbd2cabd3e21)

  ![mặt trước STM32F429-DISC1](https://github.com/user-attachments/assets/9e90f84e-d338-453d-85de-97f533ccc272)
  ![mặt trước STM32F429-DISC1 phần nút bấm](https://github.com/user-attachments/assets/ec7a1ae9-0857-4224-b597-055bd47dceb7)
  ![mặt trước STM32F429-DISC1 phần cổng Mini USB](https://github.com/user-attachments/assets/ef39afee-f989-4f53-afec-c86cf07ba21e)
  và dây Mini USB để nạp chương trình\
  ![Mini USB](https://github.com/user-attachments/assets/99d5363e-bfc9-40e1-bec6-ecdf675a64fc)

## Phần mềm STM32 CubeIDE

Dùng để lập trình cho STM32F429-DISC1

### Cài đặt phần mềm STM32 CubeIDE
 
STM32 CubeIDE là giao diện lập trình, debug, và biên dịch cho các MCU dòng STM32. Đây cũng là phần mềm chính sử dụng trong **Thực hành** của học phần.
1. Tải về bộ cài đặt ở [homepage của phần mềm](https://www.st.com/en/development-tools/stm32cubemx.html#get-software), hoặc từ bộ tải về từ [link sau](https://husteduvn.sharepoint.com/:u:/s/HnhngIT4210-2024.2/ESNGgEjq0cxHl7lqpJVtXU0Bm_i1ZSXjTgporS81Oi3z-w?e=x3oCWR).
> Chú ý: Bộ cài nặng 1GB. Việc cài đặt qua homepage sẽ cần đăng kí email, và có thể chọn phiên bản WindowsOS, Linux, hoặc MacOS.
2. Cài chương trình đơn giản, như trong hướng dẫn. Chỉ cần xem từ giây thứ 15 tới 1:05 phút. \
[![Video hướng dẫn](https://github.com/user-attachments/assets/fa34bf56-828b-4e7d-a0da-3cbddcfbae02)](https://youtu.be/CJbSfO6rkEk?si=NN-sCUCKCnF0A2We&t=15)
> Chú ý: Hãy tiếp tục chạy phần mềm và tạo một dự án demo như hướng dẫn bên dưới. Lý do là chương trình sẽ yêu cầu tạo tài khoản truy cập và tự động tải về thêm các soft package __vài trăm MB__ khá nặng. Nên thực hiện trước khi đến lớp. 
3. Chạy phần mềm STM32 CubeIDE
4. Đăng nhập vào tài khoản MyST để tải về các gói còn lại. Trên thanh menu chọn __Help/STM32 Cube updates/ Connection to MyST__
   ![image](https://github.com/user-attachments/assets/8d0a8fe4-7223-4ccf-b7f6-f7413901240c)
6. Hoàn thành các bước [tạo một dự án dưới như bên dưới](#tạo-dự-án-mới-với-stm32-cubeide). Lúc này sẽ kích hoạt các quá trình update thêm gói để **Generate Code**
> Chú ý: Nếu không hoàn thành bước __Đăng nhập__ và __Update các gói__ thì chương trình chính sẽ chỉ gồm một file .ioc duy nhất mà không có bất cứ file nội dung nào khác.

### Tạo dự án mới với STM32 CubeIDE
  [Video minh họa](https://youtu.be/iNICh5uWPAE)\
  [![thumbnail](https://github.com/user-attachments/assets/a94c4d47-ae35-493e-ba66-fdd838403d2c)](https://youtu.be/iNICh5uWPAE)
1. Chạy phần mềm STM32 CubeIDE
2. Ở menu trái, chọn **Start new STM32 project**.\
   ![image](https://github.com/user-attachments/assets/23fde9ed-cc14-4f17-b102-3899a4607010)
3. Cửa sổ **STM32 Project** được mở. Chọn tab **Board Selector**.
   Ở mục **Board Filters**, trong phần **Commercial Part Number** tìm cụm từ ***STM32F429I-DISC1***
   Ở góc dưới bên phải, bấm **Next**
   ![Chọn board STM32F429-DISC1](https://github.com/user-attachments/assets/8fe2d421-d98e-4cbc-8407-2dac21b4a179)
4. Cửa sổ **STM32 Project** thay đổi giao diện mới.
   Nhập **Project Name**.
   Bấm **Next**.
   ![image](https://github.com/user-attachments/assets/8a124016-773f-4fc6-afca-b706b556ce8c)

   > Chú ý: Cảnh báo như trong ảnh dưới có thể bỏ qua.\
   ![image](https://github.com/user-attachments/assets/d7f40dbb-9137-484d-b19b-be71f9e4e356)
5. Dự án mới, với mục tiêu làm **đèn led nhấp nháy**, đã được tạo.\
   ![image](https://github.com/user-attachments/assets/ba95e5b3-246c-4fc2-8eea-615f655264a3)

6. Ở cửa sổ __Project Explorer__ bên trái, click file __.ioc__ của dự án
7. Trong cửa sổ __Pinout & Configuration__, trong tab __Categories__, ở mục __System Core__, bấm chọn __GPIO__.\
   Ở giữa màn hình, trong phần __GPIO Mode and Configuration__ sẽ nhìn thấy danh sách các chân GPIO đã cài đặt sẵn phù hợp với board đã chọn
   ![Porting](https://github.com/user-attachments/assets/4624e85c-9bb6-4128-8864-2eb3a96124ca)
   > Cách khác là ở phần bên phải, bấm __Pinout view__, sau đó tìm và bấm vào chân GPIO trên hình mô phỏng.\
   ![Pintout view / System view](https://github.com/user-attachments/assets/f2741dc3-0f4b-4a1d-8b44-559f9d227155)
8. Nếu cần hiệu chỉnh các chân GPIO thì thực hiện.\
   Nếu không, cứ bỏ qua.
10. Trên thanh __menu bar__, chọn __Project__, bấm __Generate Code__
    ![Generate Code](https://github.com/user-attachments/assets/1da13016-0159-424e-9a19-e250f3b9948e)



## Breadboard cắm dây

- Mini breadboard SYB-170:
  - Giả lập wowki minh họa cách sử dụng kết hợp 2 mini breadboard: <https://wokwi.com/projects/396940585346083841>\
    ![image](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/34a9ff24-c26e-43af-a0c6-327662c9aa9c)
  - Cấu trúc: từng nhóm 6 lỗ nối thông với nhau \
    ![Mini breadboard](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/9f83dd84-c99b-4f35-8837-393ebaae158b)\
  - Kết hợp 2 breadboad mini để cắm MCU - nhìn từ trên xuống \
    ![image](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/95f91b6f-3e55-4412-992e-e2106beafbe5)
  - Kết hợp 2 breadboad mini để cắm MCU - nhìn từ cạnh bên \
   ![image](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/aee0ed03-ccf7-4607-ae0e-6e12e481eaa2)
- Half breadboard:
  - Giả lập wowki minh họa cách sử dụng kết hợp 2 half breadboard: <https://wokwi.com/projects/396941371646011393>\
    ![image](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/5a61cbca-9fb3-4176-9c65-694433929df0)
- Breadboard:
  - Giả lập wowki minh họa cách sử dụng breadboard: <https://wokwi.com/projects/396941799195558913>\
    ![image](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/1ef63610-c6c6-43dc-ba9c-fb9c4262fab4)
- Breadboard Sunhayato SAD-12
    ![image](https://github.com/neittien0110/SOICT_HeNhung/assets/8079397/6da38f41-f17d-4d17-aa1a-944694943e93)

- Tham khảo: <https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard/all>

## Các bài thực hành

### Nháy đèn buit-in LED trên board

 Xem ở phần[Tạo dự án mới với STM32 CubeIDE](#tạo-dự-án-mới-với-stm32-cubeide)

### Mở rộng - Nháy đèn LED lắp ngoài

 ![image](https://github.com/user-attachments/assets/a07cefcb-a14f-4e6c-b843-43cc4c3b74cf)

- Bước 1: giữ phần mềm + thêm phần cứng
  - Giữ nguyên phần mềm của của bài [Nháy đèn buit-in LED trên board](#nháy-đèn-buit-in-led-trên-board)
  - Lắp breadboad với led và điện trở, đấu nối với các chân PG13, PG14 (cùng chân PIN với built-in led trên board)
  - Kết quả mong đợi: đèn led built-in và led ngoài nhấy nháy giống hệt nhau
- Bước 2: đổi phần mềm + giữ phần cứng
  - Giữ nguyên breadboard như ở bước 1
  - Cấu hình lại phần mềm, không sử dụng chân PG13, PG14 nữa mà dùng chân PIN khác tùy chọn.
  - Kết quả mong đợi: led ngoài vẫn nhấy nháy giống như ở bước 1.
- Minh họa trên wowki: <https://wokwi.com/projects/396942366366011393>

