# K-NET

[knet-kwu.github.io](https://knet-kwu.github.io/)

PR 하기 전에 랜더링이 잘 되는지 확인하자

> bundle exec jekyll serve

## 글 작성

`/_posts`에 마크다운 형식으로 작성

마크다운이나 다른 기능들 정리한 것은 [작성-방법](./_posts/2021-12-07-작성-방법.md)에 정리했으니 참고

글 작성시 마크다운 파일 이름 형식 : `2019-08-21-This-is-my-blog-post.md`

```md
---
layout: post
title: 제목
hide_title: false # Hide the title when displaying the post, but shown in lists of posts
feature-img: "assets/img/sample.png" # 크게 보이는 이미지 (대문)
thumbnail: "assets/img/thumbnails/sample-th.png" # 썸네일 이미지
color: rgb(80,140,22) # Add the specified color as feature image, and change link colors in post
bootstrap: true # Add bootstrap to the page
tags: [sample, markdown, html] # 태그 만든것 다는 것
---
```

## 사진 추가

사진은 사진의 용도에 따라서 폴더에 분류해서 넣으세요

예를 들어, 2022년 1차 컨퍼런스 폴더에 사진 모두 넣기 X

사진은 assets/img  

1. 사진 여러개 격자 배열로 넣는 경우, aligner.html 사용

이미지 파일 경로 접두사 'assets/img' 경로가 접두사 붙어짐

사용 예시)

```/path/to/image.png```

```{% include aligner.html images="posts/path/to/image1.png ,posts/path/to/image2.png" column=2 row=1 %}```

2. 사진 하나 + 설명 추가하는 경우, image.html 사용

개인적으로 만든 html 파트입니다.

사용 예시)

```/assets/img/path/to/image.png```

```{% include image.html src="/assets/img/posts/about_minecraft/servers.png" caption="이미지 하단에 첨부할 내용" %}```

### 갤러리에 추가하는 경우

갤러리에 생성되는 HTML 요소는 자동으로 랜더링 되는 형식으로 `/assets/img/pexels`에 넣으면 된다.

### 포스트에 글에 첨부하는 경우

원하는 이미지의 경로를 마크다운 형식으로 작성하면 된다.

```md
![이미지 대체 택스트-간단한 설명](경로)
```

## 프로젝트 추가

`/_portfolio`에 진행중인 프로젝트의 간단한 설명과 함께 마크다운 형식으로 작성

## 블로그 하단에 바로가기 아이콘

`/_data/icons.yml`에 작성
