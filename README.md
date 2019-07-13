# face_recognition

-----------------------------------------------------------------------------------------------

## 專案的檔案路徑佈局
1.在face-recognition的目錄裡產生二個子目錄data與model  
2.從[Labeled Faces in the Wild資料集官網]點撃[All images as gzipped tar file](http://vis-www.cs.umass.edu/lfw/lfw.tgz)來下載lfw.tgz。    
3.解壓縮lfw.tgz到face-recognition/data/的目錄下   
4.執行face-detect-align-and-crop.ipynb來進行臉部偵測、對齊 & 裁剪    
5.下載Facenet模型檔[20170511-185253.zip(168M)](https://drive.google.com/file/d/0B5MzpY9kBtDVZ2RpVDYwWmxoSUk)並解壓縮到"model/facenet"的目錄下。  
6.在"model"的目錄下產生一個子目錄"svm"來存放"人臉分類器"的模型。  
7.執行face-embedding-and-recognition-classifier.ipynb來進行人臉特徵擷取(FaceNet) & 訓練人臉分類器    
8.在"data"的目錄下產生一個子目錄"test"來存放"人臉辨識"用的測試圖像 

----------------------------------------------------------------------------------------------
## 檔案路徑:
<pre><code>face-recognition/  
├── 01-face-detect-align-and-crop.ipynb  
├── 02-face-embedding-and-recognition-classifier.ipynb  
├── 03-face-classification.ipynb  
├── detect_face.py  
├── facenet.py  
├── visualization_utils.py  
├── model/  
│	├── svm/                                <--- 人臉分類器(svm)的模型  
│	│	└── lfw_svm_classifier.pkl  
│   ├── mtcnn/  
│   │   ├── det1.npy    
│   │   ├── det2.npy      
│   │   └── det3.npy      
│   └── facenet/                            <--- Facenet的模型     
│   └── 20170512-110547/    
│          ├── 20170512-110547.pb   
│          ├── model-20170512-110547.ckpt-250000.data-00000-of-00001    
│          ├── model-20170512-110547.ckpt-250000.index  
│          └── model-20170512-110547.meta   
└── data/   
    ├── test/   
    ├── lfw/    
    │   ├── Aaron_Eckhart/        
    │   │   └── Aaron_Eckhart_0001.jpg  
    │   ├── ...     
    │   └── Zydrunas_Ilgauskas/     
    │       └── Zydrunas_Ilgauskas_0001.jpg     
    └── lfw_crops/                          <--- 經過偵測、對齊 & 裁剪後的人臉圖像     
        ├── Aaron_Eckhart/        
        │   └── Aaron_Eckhart_0001.png  
        ├── ...     
        └── Zydrunas_Ilgauskas/     
            └── Zydrunas_Ilgauskas_0001.png</pre></code> 
