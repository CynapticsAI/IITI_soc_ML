## **IITIsoc Project: Sign Language Translator**

---
### **Contents**
- [Introduction](#Introduction)
- [Preview](#Preview)
- [Run](#Run)
- [Demo](#Demo)
- [Inference](#Inference)
- [Training](#Training)
- [Accuracy measures](#Accuracy-measures)
- [Dataset used](#Dataset-used)
- [Other Models Tried](#Other-Models-Tried)
- [Documentation](#Documentation)
- [References](#References)

### **Introduction**
In this presentation, we will be demonstrating a Computer Vision demo using YOLOv5 on the American Sign Language Dataset including 26 classes.The model identifies signs in real time as well as with input image or audio and builds bounding boxes showing label with confidence value..The model is showcased using streamlit which can take input as an image.

---

### **Preview**

Sign Language Detection Using YOLO Algorithm

<img width="400" src="https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/Demo/WIN_20220811_16_28_57_Pro.jpg">

<img width="400" src="https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/Demo/WIN_20220811_15_23_17_Pro.jpg">

<!-- ![res-2](https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/Demo/WIN_20220811_16_28_57_Pro.jpg) -->


**Yolo model:**
You Only Look Once (YOLO) family of detection frameworks aim to build a real time object detector, which what they lack in small differences of accuracy when compared to the two stage detectors, are able to provide faster inferences.It predicts over limited bounding boxes generated by splitting image into a grid of cells, with each cell being responsible for classification and generation of bounding boxes, which are then consolidated by NMS.

**YOLOv5 architecture:**

![alt text](https://blog.roboflow.com/content/images/2020/06/image-11.png)



---
### **Run**
Clone the repo in virtual environment and open the website using the following command:
```bash
streamlit run app.py
```

[Follow the link and input image or video. It will return the file with signs identified along with the confidence value.]: #



 
---
### **Demo**
<video src='https://user-images.githubusercontent.com/107802412/184130019-2472c959-ec44-4211-91a5-9ce838633cf3.mp4' width="400"></video>

<video src='https://user-images.githubusercontent.com/107802412/184349579-101a7631-f1bc-4924-b156-528c910b2aea.mp4' width="400"></video>
 



### **Inference**

<details open>
<summary>Install</summary>

Clone repo and install [requirements.txt](https://github.com/snarkyidiot/IITI_soc_ML/blob/f8e1d24659ff3181d133d9c2f575c2b816de4c1a/requirements.txt) in a
[**Python>=3.7.0**](https://www.python.org/) environment, including
[**PyTorch>=1.7**](https://pytorch.org/get-started/locally/).

```bash
git clone https://github.com/snarkyidiot/IITI_soc_ML.git  # clone
cd yolov5
pip install -r requirements.txt  # install
```

</details>

<details open>
<summary>Inference</summary>


- You can run inference inside YoloV5_main folder by using this command:
 

    ```bash
    python detect.py --source 0  # webcam
                              img.jpg  # image
                              vid.mp4  # video
                              path/  # directory
                              path/*.jpg  # glob
                              'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                              'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
    ```
- The results are saved to `runs/detect`

</details>

---
### **Training**
Tensorboard results:
<img width="800" src="https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/Demo/results.png">
https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/exp3/results.csv
for details on each epoch

---

### **Accuracy measures**

On testing our model on our testing dataset it returned the following metrics
- Precision:0.983
- recall:0.987
- F1Score:0.985
- mAP@.5:0.993
- mAP@.5:.95: 0.84
- Accuracy: 0.989
- for class wise detail refer this:
https://docs.google.com/spreadsheets/d/1vNaIl_QhOzDW6Ybr08uVx-mlAI5BWqOOxjPJnY_aVR8/edit#gid=0
---


### **Dataset-used**
We have used an American Sign Language Dataset consisting of 3399 images having 26 American Sign language alphabets. This dataset was used because of the availability of annotations which were required for training our YOLO-v5s model.
* [American Sign Language](https://universe.roboflow.com/sign-language/american-language/dataset/1)

---
### **Other Models Tried**

-  [![Open All Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1dEI4jfkUO9_u5NLw_FQ-8ute53WbU_eg?usp=sharing) (Model using CNN layers for real time sign language detection))

-  <img src="https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/Demo/Screenshot%20(887).png" width="250"/>

<br/><br/>




-  [![Open All Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1syYyApJSgzV6S0ZIZ5aRLvsN5espFHM1?usp=sharing)(Model uses holistic mediapipeline)

-  <img src="https://raw.githubusercontent.com/snarkyidiot/IITI_soc_ML/main/Demo/WhatsApp%20Image%202022-08-12%20at%203.05.10%20PM.jpeg" width="250"/>

----

### **Documentation**

See the [Sign language translator doc](https://docs.google.com/document/d/1quMYLkYbuVvIrYl0c2jhnK0RxlBHqOovEMcEK7WBfMo/edit?usp=sharing) for full documentation on implementation of models and deployment.


---

### **References**

* https://github.com/ultralytics/yolov5
* https://github.com/roboflow-ai
* https://zone.biblio.laurentian.ca/bitstream/10219/3843/1/Thesis%20FINAL%20-%20Devina%20Vaghasiya%20-%2025-Mar-2021.pdf
*  https://docs.ovh.com/asia/en/publiccloud/ai/training/web-service-yolov5/


***Thanks for Reading***

---


<!-- 
https://user-images.githubusercontent.com/107802412/184129250-b72b0c76-0256-49f3-b9e9-6106d6437897.mp4



https://user-images.githubusercontent.com/107802412/184130019-2472c959-ec44-4211-91a5-9ce838633cf3.mp4 -->





