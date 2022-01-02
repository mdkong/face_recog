
```bash
./
├── 발표 순서
│   ├── 프로젝트 개요 및 개발 배경
│   └── 프로젝트 발표
│       ├── 프로그램 설명
│       └── 시연 (Demonstration)
├── 개선 및  보완 사항
└── Q&A
``` 


# 발표 순서 
- ## 프로젝트 개요 및 개발 배경
- ## 프로젝트 발표
- - ##  프로그램 설명
- - ## 시연 (Demonstration) 
- ## 개선 및 보완 사항 
- ## Q&A


# 프로젝트 개요: 
- ## Project Title: AI 기술을 활용한 얼굴인식 프로그램(웹앱) 개발 
- ## Program Name: WAIFRP (Web-based AI Face Recognition Program(WebApp))
-      Pre-Alpha Releases through Build, Test, and Deployment Automation by MD.Kong.


# 프로젝트 개요

-  AI 기술(얼굴 인식 딥러닝 모델)을 활용하여 
-  웹에서 실시간으로 카메라 영상을 입력받아 저장 후 (화면 개발)
-  입력되는 카메라 영상속 인물들 중에서 일치하는 사람을 구별해 낸다
-- Verification (검증) & Identification (식별)

# 프로젝트 개발 배경 

- Python, Flask, MySOL, HTML, CSS etc.을 이용한 웹서비스를 개발 계획
-- OpenCV, JavaScript
- Bootstrap5,  [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html) , Github, gh-pages 등을 이용하여 반응형 웹앱 개발로 변경
-- OpenCV.js: Webpage, Image Processing, Object Detection, DNN Module etc.



# 프로젝트 상세 설명

-  AI 기술(얼굴 인식 머신러닝 모델)을 활용하여 
-- weights: caffemodel (res10_300x300_ssd_iter_140000_fp16.caffemodel)
--  cf. tensor model 
-- Recognition Model: openface.nn4.small2.v1.t7
-- Config: deploy_lowres.prototxt
-  웹에서 카메라 영상을 직접 입력받아 저장 후 
- 실시간으로 입력되는 카메라 영상속 인물들 중에서 일치하는 사람을 구별해 낸다
-- Bootstrap5 (화면 개발)
-- OpenCV.js (얼굴인식 프로그램 포팅)



## 개발에 사용된 자원들 (Resources)

WAIFRP 개발에 사용된 자원들의 상세한 설명은 아래 링크된 사이트 참조

| Resources | README |
| ------ | ------ |
| Bootstrap | [https://getbootstrap.com/docs/5.0/getting-started/introduction/][PlMe] |
| OpenCV.js | [https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Colab | [https://colab.research.google.com/][PlOd] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |




# 프로그램 소개 

>- 아래 코드 참조 
-- https://github.com/mdkong/cv_face_recog/blob/main/index.html
- 프로그램 실행 데모
-- https://mdkong.github.io/cv_face_recog/



# 추후 보완 내용:

>- 좀 더 정확한 모델 선정 및 다양한 기능을 포함한 화면 구성
-- tensorflow.js model test

>- 안드로이드 플랫폼에서의 패키징 처리하여 앱 배포 구현 (플레이스토어에 배포)
- 3D 기능 구현한 라이브러리 (WebAR, WebVR 등) 활용한 앱 개발



>
> 감사합니다


