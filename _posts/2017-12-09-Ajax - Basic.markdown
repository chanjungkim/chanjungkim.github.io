---
layout: post
title:  Ajax - Basic
date:   2017-12-09 12:19:00
author: C-an
categories: Jekyll
---

<!-- Contents -->

In this post, I am gonna decribe about ajax in Spring.

This is tis simple form.
```javascript
...
	$.ajax({
        type : 'POST',
        url : 'write.do',
        data : {
            'article_num' : article_num,
            'userId' : memberId
        },
        dataType : 'json',
        success : function (resultData){
            // Describe what this page should do after sucess.
            // adding & removing tags that should happen after refreshing the page.
        },
        error : function(){
            alert('Error Message')
        }
    })
...
```
`type` is the method you send it to its server(controller). GET, POST, PUT, DELETE, HEAD. But Other than GET and POST. They are not used a lot.

`url` is the rule of address in the server(controller) of the Spring project.

`data` is the data that you send to its server(controller).
You can write it like this too.

`dataType` is the type that the page would recieve.

`async` is checking true(async) or false(sync).

You can recieve the parameters like this. Using Gson is nice to return an Object in JSON form.

```java
@RequestMapping(value = "/write.do", method=RequestMethod.POST)
public void writePost(..., String userId) {
    try {
        writer = response.getWriter();
        Gson gson = new Gson();
   	 writer.print(gson.toJson(leftArticleNum));
    } catch (IOException e) {
        // TODO Auto-generated catch block
        e.printStackTrace();
    }
}
```
If you create a Gson Object, it make an object into JSON form automatically.