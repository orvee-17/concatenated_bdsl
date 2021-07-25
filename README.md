# Bangla Sign Language Recognition Using Concatenated BdSL Network
This repository contains the Tensorflow implementation of our model "Bangla Sign Language Recognition Using Concatenated BdSL Network" <br>
[[Code](https://github.com/orvee-17/concatenated_bdsl)] 

<!-- ![Main Model](sample_pictures/main.png "SSVC Architecture")
 -->
## Authors
   [Thasin Abedin](https://github.com/orvee-17), [Khondokar S. S. Prottoy](), [Ayana Moshruba](), [Safayet Bin Hakim]()

## Requirements
Install the following dependencies before running the model
  - Tensorflow 2.2 `pip install tensorflow == 2.2`
  - tqdm `pip install tqdm`
  - sklearn `pip install -U scikit-learn`

## Directory structure
```
-root
  -image_only_network.ipynb
  -main.ipynb
  -numpy_conversion.ipynb
  -pretrained_openpose.ipynb
  -bangla_dataset
    -np_files
      -imglist_t.npy
      -imglist_v.npy
      -labellist_t.npy
      -labellist_v.npy
      -poselist_t.npy
      -poselist_v.npy      
    -train
    -test
    -validate
  -hand_models
    -pose_deploy.prototxt
    -pose_iter_102000.caffemodel (Download this pretrained file)
```

## Train and Evaluate
  - Download and extract 'pose_deploy.prototxt' and 'pose_iter_102000.caffemodel' and put them in 'hands_model' folder.
  - Download the [MSVD](https://www.microsoft.com/en-us/download/details.aspx?id=52422&from=https%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fdownloads%2F38cf15fd-b8df-477e-a4e4-a4680caa75af%2F) dataset. Split the data in train-test-val sets.
  - Run the numpy_conversion.ipynb file first. This makes the numpy files for images, labels and pose estimations for train, test and validation sets and saves them in 'np_files' folder.
  - After that run the main.ipynb file to train the 'Concatenated BdSL Network' and save the weights in 'file_weights' folder. The validation and test results can also be obtained by running this.

## Sample Outputs
<!-- ![](sample_pictures/A1_1.png "sample result 1")<br>
SSVC: "A woman is cutting a piece of meat" <br>
GT: "a woman is cutting into the fatty areas of a pork chop" <br>
SS score: 1.0, BLEU1: 1.0, BLEU2: 1.0, BLEU3: 1.0, BLEU4: 1.0<br>

![](sample_pictures/A1_2.png "sample result 2")<br>
SSVC: "A person is slicing tomato" <br>
GT: "Someone wearing blue rubber gloves is slicing a tomato with a large knife" <br>
SS score: 0.825, BLEU1: 1.0, BLEU2: 1.0, BLEU3: 1.0, BLEU4: 1.0<br>


![](sample_pictures/A1_3.png "sample result 3")<br>
SSVC: "A woman is cutting a piece of meat" <br>
GT: "a woman is cutting into the fatty areas of a pork chop" <br>
SS score: 0.94, BLEU1: 1.0, BLEU2: 0.84, BLEU3: 0.61, BLEU4: 0.0<br>
 -->
