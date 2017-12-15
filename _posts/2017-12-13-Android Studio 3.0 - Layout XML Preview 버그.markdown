---
layout: post
title: "Layout XML Preview 버그"
date:   2017-12-12 11:04:00
author: C-an
categories: Android Studio 3.0
---

##1 한글 에러##

안드로이드 3.0버전에서 한글 깨짐 문제가 개선이 되어 따로 수정하지 않아도 한글이 나온다.
하지만 이전 버전에서 작업을 한 개발자의 경우 업데이트를 하면서 Layout Preview가 안나오는 경우가 있는데 이는 이전 버전에서 한글 깨짐 때문에 Android Studio 폴더 안에 **fonts.xml** 를 수정해서 그렇다.

아래와 같은 경로에서 기존 **fonts.xml**파일을 **[fonts.xml](https://github.com/chanjungkim/chanjungkim.github.io/tree/master/_posts/downloads/androidstudio/fonts.xml)**(Click)로 덮어씌우고 안드로이드 스튜디오를 재실행하면 된다.

```
C:\Program Files\Android\Android Studio\plugins\android\lib\layoutlib\data\fonts\fonts.xml
```

##2 Hardcoded Text 에러##

기존 버전에서는 **/values/strings.xml**에 작성해야지만 세부적인 에러나 확장성을 갖게되어 **strings.xml**에 작성하였지만, 안그로이드 3.0버전에서는 작성할 필요 없이 곧바로 작성해도 에러가 뜨지 않는다. 에러가 뜨는 경우에는

```
Setting -> Search: Hardcoded Text -> 경고 체크 해제
```
로 해결한다.