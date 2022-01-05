<h1 align="center">Project PT & Demo</h1>  
<br /> 

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

<br /> 
<br /> 

# 프로젝트 개요 - Goal  1️⃣

- ## Project Title: AI 기술을 이용한 얼굴인식 프로그램(웹앱) 개발

  - ## Program Name: WAIFRP

  - Web-based AI Face Recognition Program(WebApp)
  - *Pre-Alpha Release through Build, Test and Deployment Automation by MD.Kong*

<br /> 
<br /> 

# 프로젝트 개요 - Objectives 2️⃣

- OpenCV.js로 ML 모델 빌드

- ML 모델을 웹브라우저로 배포
  - 자바스크립트를 실행할 수 있는 모든 곳에서 기존 모델 실행

<br /> 
<br /> 

# 프로젝트 개발 배경 3️⃣

- Python, Flask, MySOL, HTML, CSS etc.을 이용한 웹서비스를 개발 계획
  - OpenCV, JavaScript
- Bootstrap5,  [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html) , Github, gh-pages 등을 이용하여 반응형 웹앱 개발로 변경
  - OpenCV.js: Webpage, Image Processing, Object Detection, DNN Module etc.
  - All-in-One Github (No need of NPM,Registry, Firebase etc.)

<br /> 
<br /> 

# 프로젝트 상세 설명 🕵️

## Face Recognition Pipeline
![Face recognition pipeline](https://user-images.githubusercontent.com/77907363/147905111-5c272a23-a312-49c0-9871-e4ccacea8e28.png)


| Pipeline |Network | Comments |
| :------: | ------ |------ |
| 1 | Face Detection | 이미지에서 한 개 이상의 얼굴을 검출. BGR 이미지를 입력 받고, 얼굴이라고 생각할 수 있는 부분에  네모 박스 (Bounding Box)를 그린다    |
| 2 | Feature extraction | 얼굴 이미지에서 가장 중요한 특징들을 추출.  SSD framework (Single Shot MultiBox Detector)에 기초한  reduced ResNet-10 model 사용|
| 3 | Face classification | 추출된 특징들에 기초하여 얼굴 분류. 이 네트워크는 OpenFace라고 불린다.  96 x 96 사이즈의 RGB 얼굴 이미지를 입력받아 128차원의 단위 벡터를 리턴하며 이는 단위 다차원공간에서의 한 점으로 표기한다.  이로써 두 얼굴사이의 차이는 두 출력벡터들 사이의 거리로 판단할 수 있다([Triplet Loss Function](https://tech.kakaoenterprise.com/63)) |

  - weights: caffemodel.SSD
[res10_300x300_ssd_iter_140000_fp16.caffemodel](https://medium.com/acm-juit/ssd-object-detection-in-real-time-deep-learning-and-caffe-f41e40eea968)

  - Config: [deploy_lowres.prototxt](https://fileinfo.com/extension/caffemodel)
 
  - Recognition Model: [openface.nn4.small2.v1.t7](https://cmusatyalab.github.io/openface/#overview)

<br /> 
<br /> 

## 코딩 요구사항 📈
- AI 기술(얼굴 인식 딥러닝 모델)을 이용하여
  - DNN 모델 선정 및 준비 (Caffemodel, OpenFace etc.)
  
- 웹에서 실시간으로 카메라 영상을 입력받아 그 중에서 사람의 얼굴 부분을 추출 및 저장하고 
  - Localization, IoU
  - Object Detection, Feature map 생성
 
- 기준(anchor)이 되는 얼굴과 일치할 가능성이 높은 얼굴을 구별해 낸다
  - Identification (식별), Verification (검증)


<br /> 
<br /> 

## 개발에 사용된 자원들 (💠🔶Resources)

| Resources | Use | README |
| ------ | ------ |------ |
| Bootstrap | 페이지 작성 | [https://getbootstrap.com/docs/5.0/getting-started/introduction/] |
| OpenCV.js | 핵심 기능 모듈 | [https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html] |
| GitHub | Registry, 웹호스팅 & 배포 | [https://github.com/mdkong/face_recognition_w_opencvjs#readme] |
| Colab | IDE | [https://colab.research.google.com/] |
| Google Drive | DB | [https://www.google.com/drive/] |


<br /> 
<br /> 

## 소스 코드
  - [소스코드 보기](https://github.com/mdkong/face_recognition_w_opencvjs/blob/main/index.html)

<br /> 
<br /> 

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


<br /> 
<br /> 

## 프로그램 데모
  - [프로그램 실행하기: Demo](https://github.com/mdkong/face_recognition_w_opencvjs/blob/main/index.html)

<br /> 

<br /> 

# 추후 보완 내용 🛠️ 👷

- 다양한 모델 및 파라메터를 변경하면서 테스트 해 볼 필요
  - tensorflow.js model, YOLO etc.
  
- 다양한 기능을 포함한 Interface 개선 및 화면 구성

- 안드로이드 플랫폼에서의 패키징 처리 및 배포 (플레이스토어에 배포)
- 3D 기능 구현한 라이브러리 (WebAR, WebVR 등) 활용한 앱 개발  
  


<br /> 

<br /> 

<br /> 

<br /> 

---  

감사합니다 💚

Many Thanks to @github & all the Open Source Maintainers from the bottom of my heart 👍👏
---

