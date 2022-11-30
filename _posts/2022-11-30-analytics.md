---
layout: post
title: analytics
date: 2022-11-30
comments: true
---

1. 구글 애널리틱스에 가입하고 고유의 tracking code를 받는다.

2. *inculdes* 폴더에 *google_analytics.html* 파일을 만들고 다음과 같은 코드를 작성한다.

```
<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-250483978-1', 'auto');
  ga('send', 'pageview');
</script>
```

여기서 'UA-250483978-1'가 나의 tracking code다.

3. *_config.yml* 파일을 열고 다음의 코드를 추가한다.

```
google_analytics: "UA-250483978-1"
```

4.  *head.html*에 다음의 코드를 추가한다.
```
{% if site.google_analytics and jekyll.environment == 'production' %}
    {% include google_analytics.html %}
```

5. 완성
[analytics]