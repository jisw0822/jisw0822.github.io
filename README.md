# Project Build Process

## Ready

1. Github에서 **jisw0822.github.io** 이름의 Repository 생성

2. `git clone`으로 로컬과 연동

3. PAT 생성

4. Window를 사용하므로, Ruby 설치

5. `gem install jekyll bundler`로 지킬 설치

*이후 시행착오를 통해 같은 과정을 반복하였으므로 가장 최근에 build한 과정을 기술함*


## Build Jekyll Project 

1. 현재 디렉토리(jisw0822.github.io)에 `jekyll new . --force`로 Jekyll 설치


## Add Theme

1. [Lanyon](https://github.com/poole/lanyon) 테마에서 Download ZIP 을 통해 로컬 저장소(jisw0822.github.io)에 파일 저장

2. *_config.yml* 파일에서 블로그 이름 등 기본 정보를 변경

3. *default.html* 파일에서 `<body class="theme-base-0b">` 코드 추가를 통해 테마 색상 변경

3. `git add`, `git commit -m "메세지"`, `git push origin main` 등의 명령을 통해  변경사항을 git에 반영


## Add Comment Function

1. Disqus 가입 및 Universal Code 복사

2. *_config.yml* 파일에 다음과 같은 코드 작성 

```
comment:
  provider:        "disqus"
  disqus:
    shortname:     "jisw0822" 
```

3. *_layouts/post.html*에 Universal Code 복사 및 PAGE_URL과 PAGE_IDENTIFIER 설정

4. post에 `comments: True` 지정


## Update Post

1. *_posts* 폴더에 .md 형식의 파일을 추가 및 수정하여 포스트 작성

2. `git add`, `git commit -m "메세지"`, `git push origin main` 등의 명령을 통해  변경사항을 git에 반영