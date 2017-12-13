---
layout: post
title: "Layout XML Preview 버그"
date:   2017-12-12 11:04:00
author: C-an
categories: Android Studio 3.0
---

안드로이드 3.0버전에서 한글 깨짐 문제가 개선이 되어 따로 수정하지 않아도 한글이 나온다.
하지만 이전 버전에서 작업을 한 개발자의 경우 업데이트를 하면서 Layout Preview가 안나오는 경우가 있는데 이는 이전 버전에서 한글 깨짐 때문에 Android Studio 폴더 안에 **fonts.xml** 를 수정해서 그렇다.

아래와 같은 경로에서 [fonts.xml](./downloads/androidstudio/fonts.xml)(Click)으로 덮어씌우고 안드로이드 스튜디오를 재실행하면 된다.

```
C:\Program Files\Android\Android Studio\plugins\android\lib\layoutlib\data\fonts\fonts.xml
```