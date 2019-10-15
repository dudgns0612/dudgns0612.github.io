---
layout: post
title: "[Mybatis] Mybatis를 이용한 Mapper 사용 시 CamelCase(카멜케이스)자동변환"
excerpt: "Mybatis 사용 시 Mapper에서 변수명 자동 CamelCase변환 옵션주기."
categories: [Mybatis]
date: 2017-06-01
modified: 2017-06-01
comments: true
---

Mapper에서 Vo나 필요한 Map 클래스에 사용하기위해 CamelCase로 변환해주어야 한다 <br />
이때 수동으로 변환이 가능하지만 Mybatis옵션을 통하여 자동으로 변환하게 해줄수 있다. <br />
설정하여 놓았던 mybatis-config.xml 에 이와같이 추가해주면 자동으로 변환이 될 수 있다. <br />

### Code Blocks

​Mybatis 사용 시 Mapper에서 변수명 자동 CamelCase변환 옵션주기.<br />

{% highlight xml %}
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE configuration
PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
    "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
    <settings>
        <!-- 자동으로 카멜케이스 규칙으로 변환 -->
        <setting name="mapUnderscoreToCamelCase" value="true"/>
    </settings>
</configuration>
{% endhighlight %}

### Additional Description

참조 : 더많은 mybatis 옵션 보기 <br />
[http://www.mybatis.org/mybatis-3/ko/configuration.html](http://www.mybatis.org/mybatis-3/ko/configuration.html)
