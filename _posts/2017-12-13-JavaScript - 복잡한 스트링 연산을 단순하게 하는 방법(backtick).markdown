---
layout: post
title: "JavaScript - 복잡한 스트링 연산을 단순하게 하는 방법"
date:   2017-12-12 11:04:00
author: C-an
categories: JavaScript
---

Backtick(백틱)이란 키보트에서 1 옆에 있는 따옴표(?) 표시를 의미한다. 영어에서 Tick이란 체크 표시를 할 때를 의미하기도 한다.

자바스크립트에서 다음과 같이 스트링 연산시 헷갈려서 엉키는 경우가 많다.

```javascript
var studentData = "<table>";

for(int i = 0 ; i < n ; i++){
	studentData += "<tr>";
    studentData += "<td>";
    studentData += student[i].name;
    studentData += "</td>";
    studentData += "<td>";
    studentData += student[i].age;
    studentData += "</td>";
    studentData += "<td>";
    studentData += student[i].grade;
    studentData += "</td>";
    studentData += "<td>";
    studentData += student[i].hobby;
    studentData += "</td>";
    studentData += "</tr>";    
}
studentData += "</table>";
```

혹은

```javascript
var studentData = "<table>";

for(int i = 0 ; i < n ; i++){
	studentData += "<tr>";
    			+"<td>";
        		+= student[i].name;
        		+= "</td>";
    			+= "<td>";
            	+= student[i].age;
    			+= "</td>";
    			+= "<td>";
    			+= student[i].grade;
    			+= "</td>";
    			+= "<td>";
    			+= student[i].hobby;
    			+= "</td>";
    			+= "</tr>";    
}
studentData = "</table>";
```
와 같이 사용할 것이다. 하지만 Backtick을 사용하면 다음과 같이 좀 더 간결하게 할 수 있다.

```javascript
var studentData = "<table>";

for(int i = 0 ; i < n ; i++){
	studentData += `<tr><td>${student[i].name}</td><td>${student[i].age}</td><td>${student[i].grade}</td><td>${student[i].hobby}</td></tr>`;    
}

studentData += "</table>";
```

**주의할 점**은 **JSP** 작업 시 **EL**과 작성법이 같기 때문에 변수가 겹치지 않도록 해야한다.