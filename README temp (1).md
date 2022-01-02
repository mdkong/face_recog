# 발표 목차 
- ## 프로젝트 개요 및 개발 배경
- ## 프로젝트 발표
- - ##  프로그램 설명
- - ##  시연
- ## 보완 사항 
- ## Q&A


# 프로젝트 개요: 
- ## Project Title: AI 기술을 활용한 얼굴인식 프로그램(웹앱) 개발 
- ## WAIFRP (Web-based AI Face Recognition Program(WebApp))
-      Developed by MD.Kong & Released in Dec. 2021.


[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://mdkong.github.io/cv_face_recog/)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

- ✨Magic ✨

# 프로젝트 개요

-  AI 기술(얼굴 인식 머신러닝 모델)을 활용하여 
-  웹에서 카메라 영상을 직접 입력받아 저장 후 (화면 개발)
-  실시간으로 입력되는 카메라 영상속 인물들 중에서 일치하는 사람을 구별해 낸다

# 프로젝트 개발 배경 

- Python, Flask, MySOL, html etc,을 이용한 웹서비스를 개발 계획
-- CSS, OpenCV, JavaScript
- Bootstrap5, OpenCV.js, Github, gh-pages 등을 이용하여 반응형 웹 개발로 변경
-- OpenCV.js: Webpage, Image Processing, Object Detection, DNN Module etc.
- IDE: Colab with GPU


# 프로젝트 상세 설명

-  AI 기술(얼굴 인식 머신러닝 모델)을 활용하여 
-- weights: caffemodel (res10_300x300_ssd_iter_140000_fp16.caffemodel)
-- Recognition Model: openface.nn4.small2.v1.t7
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

- 아래 코드 참조
-- https://github.com/mdkong/cv_face_recog/blob/main/index.html
- 프로그램 실행 데모
-- https://mdkong.github.io/cv_face_recog/


# 추후 보완 내용:

- 좀 더 정확한 모델 다양한 기능을 포함한 앱 개발
- 안드로이드 플랫폼에서의 패키징 처리하여 앱 배포 구현 (플레이스토어에 배포)
- 3D 기능 구현한 라이브러리 (WebAR, WebVR 등) 활용한 앱 개발


Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
