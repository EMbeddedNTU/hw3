# hw3

## 組員
b09901052 劉承亞  
b09901058 邱奕翔

## 使用工具
BLE TOOL (Android App)  
Raspberry Pi

## 實驗步驟(BLE TOOL部分)
1. 點開APP後點選Gatt Server
2. 右上角三個點點開選擇set Service
3. 為了方便觀察可以只留下0xfff1此Characteristic以及0x2902此Descriptor(Property勾選Notify)，並按下Apply  
![image](https://github.com/EMbeddedNTU/hw3/blob/main/312324451_649188806595596_8771190100617861702_n.jpg)
4. 按下Start Advertising

## 實驗步驟(Raspberry Pi部分)
1. 首先在Raspberry上clone下來此Repository
2. 下載bluepy  
sudo apt install python3-pip;sudo apt install libglib2.0-dev;sudo pip install bluepy
3. 移動到hw3資料夾  
cd hw3
4. 執行程式  
sudo python ble_scan_connect.py
5. 查看裝置列表並輸入您手機的裝置代號

## 實驗結果
![image](https://github.com/EMbeddedNTU/hw3/blob/main/312108082_527038335932362_5575688095424569996_n.jpg)  
由上圖可以看出有收到更改CCCD值的請求，但實際上由於BLE TOOL本身的原因並未實際修改成功