# face_recognition


檔案路徑:
face-recognition/
├── 01-face-detect-align-and-crop.ipynb
├── 02-face-embedding-and-recognition-classifier.ipynb
├── 03-face-classification.ipynb
├── detect_face.py
├── facenet.py
├── visualization_utils.py
├── model/
│   ├── svm/                                <--- 人臉分類器(svm)的模型
│   │   └── lfw_svm_classifier.pkl
│   ├── mtcnn/
│   │   ├── det1.npy
│   │   ├── det2.npy
│   │   └── det3.npy
│   └── facenet/                            <--- Facenet的模型
│       └── 20170512-110547/
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
            └── Zydrunas_Ilgauskas_0001.png
