tensorflow圖形檢測_使用Google Colab使用Tensorflow進行自定義對象檢測
--------------------------------------------------------------------
#### 跨領域-人工智慧期中報告 組員:11124110 高儒彥 11124136 王何儀

## 摘要
本報告旨在介紹如何在 Google Colab 環境中使用 TensorFlow 物件偵測 API 來構建自定義物件偵測器。我們將以蘋果圖像為範例，演示自定義對象檢測的流程，包含環境設定、資料蒐集與標註、模型訓練等主要步驟。報告內容涵蓋以下幾個主要步驟：

1. 環境安裝與設定
2. 數據集收集與標註
3. TFRecords 格式生成
4. 訓練模型配置與運行
5. 模型訓練與檢測測試
6. 推論圖生成與應用

設定Google Colab環境
------------------------------
確保您有Python 3.6或更高版本

tf-models-official 是穩定的 Model Garden 包

pip3 將自動安裝所有模型和依賴項。
```
!pip3 install tf-models-official
```
![](001.png)

如果您有可與 Tensorflow 一起使用的 GPU:
```
pip install tensorflow-gpu
```
*Other dependencies*
```
!sudo apt-get install protobuf-compiler python3-pil python3-lxml python3-tk git
!pip3 install pillow Cython lxml jupyter matplotlib contextlib2
!pip3 install --user -r models/official/requirements.txt
!pip install tensorflow-io
!pip3 install pycocotools
```
複製TensorFlow模型倉庫運行以下程式碼，克隆```TensorFlow```模型庫並進入```research```目錄：
```
!git clone https://github.com/tensorflow/models.git
```
