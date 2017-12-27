---
layout: post
title:  "Android Studio 3.0 - cancel()"
date:   2017-12-27 09:26:00
author: C-an
categories: Android_Studio_3.0
---

```java
final Dialog custom = new Dialog(this);

...

custom.cancel();
```

cancel()을 사용하기 위해서는 final 선언을 해줘야한다.