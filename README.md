# Setup nhanh react-native 0.70.2

> ## Các mục tiêu của setup

   1. Cài đặt node
   2. Cài đặt java
   3. Cài đặt yarn
   4. Cài đặt Android Sdk
   5. Cai dat thiet bi ao de phat trien
   6. Khôi phục các dependencies
   7. Build và chạy ứng dụng

> Cài đặt node

* Mở **node-v18.10.0-x64.msi** và cài đặt như thường
* Đến đoạn hỏi cài đặt Chocolatey thì bỏ tích không cần cài
* Kết thúc cài đặt, mở **cmd** hoặc **powershell**,… gõ `node -v`  

   *Kết quả*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028014631840649226/unknown.png)

> Cài đặt java

* Mở **jdk-11.0.2.7z** bằng **Winrar** hoặc **7-zip**,…
* Giải nén thư mục **jdk-11.0.2** vào chỗ nào đó. (Ở đây ví dụ này là ngay ổ C)  
![node](https://media.discordapp.net/attachments/636786976556711946/1028017024904994846/unknown.png)
* Mở thư mục **jdk-11.0.2** vừa giải nén, ta copy đường dẫn
![node](https://media.discordapp.net/attachments/636786976556711946/1028019701835636736/unknown.png)
* Mở tìm kiếm của Windows tìm **env** rồi chọn **Edit environment variables for your account**
![node](https://anakage.com/blog/wp-content/uploads/2022/02/image.png)
* Chọn **New** trong **Users variables for xxx**     
![node](https://media.discordapp.net/attachments/636786976556711946/1028021643047600258/unknown.png)
* Ô thứ nhất điền **JAVA_HOME**, ô thứ hai điền **đường dẫn lúc nãy bạn đã copy**. Bấm **OK** để lưu lại (1 lần OK thôi)
![node](https://media.discordapp.net/attachments/636786976556711946/1028022640566353940/unknown.png)
* Tiếp tục chọn **Path** trong **Users variables for xxx**. Chọn **Edit**
![a](https://media.discordapp.net/attachments/636786976556711946/1028025334928515213/unknown.png)
* Chọn **New** rồi điền **đường dẫn lúc nãy** + **\bin**. Chọn **OK** (2 lần OK)
![a](https://media.discordapp.net/attachments/636786976556711946/1028027100235575296/unknown.png)
* Kết thúc cài đặt, mở **cmd** hoặc **powershell**,… gõ `java --version`  

   *Kết quả*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028028553465442414/unknown.png)

> Cài đặt yarn

* Mở **cmd** hoặc **powershell**,... chạy `npm install -g yarn`
* Kết thúc cài đặt, mở **cmd** hoặc **powershell**,… gõ `yarn -v`  

   *Kết quả*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028029919000793208/unknown.png)

> Cài đặt Android Sdk

* Mở **Sdk.7z** bằng **Winrar** hoặc **7-zip**,…
* Giải nén thư mục **Sdk** vào chỗ nào đó. (Ở đây ví dụ này là ngay ổ C)  
![node](https://media.discordapp.net/attachments/636786976556711946/1028017024904994846/unknown.png)
* Mở thư mục **Sdk** vừa giải nén, ta copy đường dẫn
![node](https://media.discordapp.net/attachments/636786976556711946/1028031534705422346/unknown.png)
* Mở tìm kiếm của Windows, tìm **env** rồi chọn **Edit the system environment variables**  
![node](https://anakage.com/blog/wp-content/uploads/2022/02/image.png)  
* Chọn **New** trong **Users variables for xxx**   
![node](https://media.discordapp.net/attachments/636786976556711946/1028021643047600258/unknown.png)
* Ô thứ nhất điền **ANDROID_HOME**, ô thứ hai điền **đường dẫn lúc nãy bạn đã copy**. Bấm **OK** để lưu lại (1 lần OK thôi)
![node](https://media.discordapp.net/attachments/636786976556711946/1028032132112728084/unknown.png)
* Tiếp tục chọn **Path** trong **Users variables for xxx**. Chọn **Edit**
![a](https://media.discordapp.net/attachments/636786976556711946/1028025334928515213/unknown.png)
* Chọn **New** rồi điền **đường dẫn lúc nãy** + **\platform-tools**. Chọn **OK** (2 lần OK)
![a](https://media.discordapp.net/attachments/636786976556711946/1028033085025034371/unknown.png)
* Kết thúc cài đặt, mở **cmd** hoặc **powershell**,… chay `adb --version`  

   *Kết quả*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028034589823869048/unknown.png)

> Cài đặt thiết bị ảo
* Cài đặt [BlueStacks](https://www.bluestacks.com/download.html)
* Chuyển sang chế độ dọc: **Settings** -> **Display** -> **Display Resolution** -> **Portrait**   
![s](https://media.discordapp.net/attachments/636786976556711946/1028056576189276261/unknown.png)
* Bật ADB: **Settings** -> **Advanced** -> **Android Debug Bridge(ADB)**   
![w](https://media.discordapp.net/attachments/636786976556711946/1028050621401673949/unknown.png)
* Mở **cmd** hoặc **powershell**,... chạy `adb connect 127.0.0.1:5555`
* Kết thúc cài đặt, chạy tiếp `adb devices`   

   *Kết quảc trạng thái device là OK*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028056013678587904/unknown.png)

> Khôi phục các dependencies
* Mở thư mục project, trên thanh địa chỉ gõ **cmd** hoặc **powershell**,... rồi nhấn **Enter**   
![](https://media.discordapp.net/attachments/636786976556711946/1028059362230550588/unknown.png)
* Kết thúc chạy `yarn install`   

   *Kết quả*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028060949426470952/unknown.png)

> Build và chạy ứng dụng
* Mở thư mục project, trên thanh địa chỉ gõ **cmd** hoặc **powershell**,... rồi nhấn **Enter**   
![](https://media.discordapp.net/attachments/636786976556711946/1028059362230550588/unknown.png)

* Chạy `npx react-native doctor`, kiểm tra kết quả setup

    *Kết quả*  
    ![node](https://media.discordapp.net/attachments/636786976556711946/1028064233474236458/unknown.png)   
**Lỗi Android SDK và Android Studio không hề ảnh hưởng**   
```⚠ Nếu bị lỗi ở mục nào thì xem lại các bước trên cho đúng rồi kiểm tra lại```   
* Bấm **Enter** để thoát

* Kiểm tra thiết bị đã sẵn sàng chưa, gõ `adb devices`   

* Khi đã setup môi trường thành công, thiết bị đã sẵn sàng, chạy `yarn android` để build và chạy ứng dụng   

   *Kết quả*  
   ![node](https://media.discordapp.net/attachments/636786976556711946/1028069074070151248/unknown.png)
