# gLTF2glbConvertor
### 本腳本參考：<br>
[GLTF_2.0格式架構說明](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#concepts) 以及現成之GLB檔案結構製作，使用GLTF 2.0之規格設計。<br>
<br>
### 目的：<br>
GLTF結構雖然是常見的，較容易觀察模型架構的檔案，但由於其結構體包含許多分散之檔案，相較於GLB來說分類儲存以及預覽較為不便，如果使用壓縮打包的形式，在手機上預覽結果則有其難度，最佳情況應該是將其轉換成GLB檔並儲存。同時，現行之GLTF轉GLB之服務大多都是網路服務，無法內嵌也無不能自動化控制。<br>
<br>
### 方法：<br>
透過重新改寫GLTF之JSON內容，包含：
1. 宣告參考素材之容量以及讀取位置。
2. 補上缺乏之標籤。

補上GLB標頭後，再將參考素材依照GLB之格式拼於JSON後即完成。<br>
<br>
### 相關說明：<br>
* GLTF：是一種由Khronos組織開發之模型資料格式，主要設計目的為降低模型大小，可彈性擴充，方便儲存以及傳輸，能夠使用WebGL/OpenGL解析，被大量用於AR領域。[詳細說明](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0)<br>

* GLB：是GLTF的另一種儲存型式，差別在於將所有GLTF之檔案組合成一個單一的二進位檔案，方便傳輸以及儲存，GLTF和GLB可以互相轉換。[詳細說明](https://wiki.fileformat.com/3d/glb/)<br>
<br>

![GLTF結構圖](https://github.com/EricHaung/gLTF2glbConvertor/blob/master/Image/2017-gltf-20-launch-2.jpg)
GLTF結構圖<br><br><br>

![GLB結構圖](https://github.com/EricHaung/gLTF2glbConvertor/blob/master/Image/glb2.png)
GLB結構圖<br>
