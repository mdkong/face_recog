<h1 align="center">Project Intro</h1>  

# 발표 순서 🥇🥈🥉


```bash
./
├── 발표 순서
│   ├── 프로젝트 개요 및 개발 배경
│   └── 프로젝트 소개
│       ├── 프로젝트 상세 설명
│       └── 시연 (Demonstration)
├── 개선 및  보완 사항
└── Q&A
```

# 프로젝트 개요 1️⃣

- ## Project Title: AI 기술을 활용한 얼굴인식 프로그램(웹앱) 개발

  - ## Program Name: WAIFRP

  - Web-based AI Face Recognition Program(WebApp)
  -     Pre-Alpha Release through Build, Test and Deployment Automation by MD.Kong


# 프로젝트 개요 2️⃣

- AI 기술(얼굴 인식 딥러닝 모델)을 이용하여
- 웹에서 실시간으로 카메라 영상을 입력받아 그 중에서 사람의 얼굴 부분을 추출 및 저장하고 
 
- 기준(anchor)이 되는 얼굴과 일치할 가능성이 높은 얼굴을 구별해 낸다
  - Identification (식별) vs Verification (검증)

# 프로젝트 개발 배경 3️⃣

- Python, Flask, MySOL, HTML, CSS etc.을 이용한 웹서비스를 개발 계획
  - OpenCV, JavaScript
- Bootstrap5,  [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html) , Github, gh-pages 등을 이용하여 반응형 웹앱 개발로 변경
  - OpenCV.js: Webpage, Image Processing, Object Detection, DNN Module etc.
  - All-in-One Github (No need of npm publish w/ npm Registry, etc.)

# 프로젝트 상세 설명 🕵️

## 프로그램 개요 📈
- AI 기술(얼굴 인식 머신러닝 모델)을 활용하여
- 웹에서 실시간으로 카메라 영상을 입력받아 저장 후
- 입력되는 카메라 영상속 objects 중에서 사람얼굴을 구별해 내고 그 중에서 일치하는 사람을 구별해 낸다
  - Bootstrap5 (화면 개발)
  - OpenCV.js (Face Recognition algorithm, Porting to Bootstrap)

## Face Recognition Pipeline
![Face recognition pipeline](https://user-images.githubusercontent.com/77907363/147905111-5c272a23-a312-49c0-9871-e4ccacea8e28.png)


| Pipeline |Network | Comments |
| :------: | ------ |------ |
| 1 | Face Detection | 이미지에서 한 개 이상의 얼굴을 검출. BGR 이미지를 입력 받고, 얼굴이라고 생각할 수 있는 부분에  네모 박스를 그린다.  confidence를 잘 선택해야 한다. 값이 커질 수록 얼굴 아닌 다른 대상이 포함 될 가능성이 높아지고, 작아지면 얼굴 선택이 안 될 수도 있다 |
| 2 | Feature extraction | 얼굴 이미지에서 가장 중요한 특징들을 추출.  SSD framework (Single Shot MultiBox Detector)에 기초한  reduced ResNet-10 model 사용|
| 3 | Face classification | 추출된 특징들에 기초하여 얼굴 분류. 이 네트워크는 OpenFace라고 불린다.  96 x 96 사이즈의 RGB 얼굴 이미지를 입력받아 128차원의 단위 벡터를 리턴하며 이는 단위 다차원공간에서의 한 점으로 표기한다.  이로써 두 얼굴사이의 차이는 두 출력벡터들 사이의 거리로 판단할 수 있다([Triplet Loss Function](https://tech.kakaoenterprise.com/63)) |

  - weights: caffemodel.SSD
[res10_300x300_ssd_iter_140000_fp16.caffemodel](https://medium.com/acm-juit/ssd-object-detection-in-real-time-deep-learning-and-caffe-f41e40eea968)

  - Config: [deploy_lowres.prototxt](https://fileinfo.com/extension/caffemodel)
 
  - Recognition Model: [openface.nn4.small2.v1.t7](https://cmusatyalab.github.io/openface/#overview)




## 개발에 사용된 자원들 (💠🔶Resources)

| Resources | Use | README |
| ------ | ------ |------ |
| Bootstrap | 페이지 작성 | [https://getbootstrap.com/docs/5.0/getting-started/introduction/] |
| OpenCV.js | 핵심 기능 모듈 | [https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html] |
| GitHub | SCM & 웹호스팅 | [https://github.com/mdkong/face_recognition_w_opencvjs#readme] |
| Colab | IDE | [https://colab.research.google.com/] |
| Google Drive | DB | [https://www.google.com/drive/] |


## 코드 참조
  - <https://github.com/mdkong/cv_face_recog/blob/main/index.html>

## 작업 폴더 목록

~~~
D:\GITHUB\FACE_RECOGNITION_W_OPENCVJS
+---.github
|   \---workflows
+---assets
|   +---brand
|   \---dist
|       +---css
|       \---js
+---data
\---js
~~~


## 프로그램 데모
  - <https://mdkong.github.io/cv_face_recog/>

# 추후 보완 내용 🛠️ 👷

- 다양한 모델 및 파라메터를 변경하면서 테스트 해 볼 필요
  - tensorflow.js model, YOLO etc.
  
- 다양한 기능을 포함한 화면 구성

- 안드로이드 플랫폼에서의 패키징 처리 및 배포 (플레이스토어에 배포)
- 3D 기능 구현한 라이브러리 (WebAR, WebVR 등) 활용한 앱 개발  
  


---  

감사합니다 💚

Many Thanks to @github & all the Open Source Maintainers from the bottom of my heart 👍👏
---

