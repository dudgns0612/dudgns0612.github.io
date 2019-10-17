---
layout: post
title: "[Mybatis] Oracle CLOB 처리 ResultMap"
excerpt: "Oracle에서 CLOB 타입을 처리하기 위해서는 resultMap 태그를 이용해서 타입을 지정해줘야 한다."
categories: [Mybatis]
date: 2017-09-04
modified: 2017-09-04
comments: true
---

Oracle DB CLOB타입 사용시 원래 기존 방식으로 불러오면 CLOB타입 자체를 가져오는 듯한 문자열이 찍히게 된다.<br />
Oracle에서 CLOB 타입을 처리하기 위해서는 resultMap 태그를 이용해서 타입을 지정해줘야 한다.<br />
CLOB 타입을 String 형태로 지정하여 주기 위함이다.<br />

### Code Blocks

​resultMap으로 지정하였을 때는 resultType이 아니라 resultMap으로 설정하여 줘야한다.<br />

{% highlight xml %}
<resultMap id="contents" type="hashmap">
  <result property="CONT" column="CONT" jdbcType="CLOB" javaType="java.lang.String" />
</resultMap>
{% endhighlight %}

### Description
설명 :  resultMap을 만들고 사용할 id는 contents , 타입은 hashMap을 사용할것이고 <br />
CLOB타입의 컬럼은 CONT라는 컬럼이며 jdbcType은 CLOB 이렇게 설정된 컬럼을 <br />
String 타입으로 인지한다라고 볼 수 있다. <br />
이렇게하면 CLOB타입으로 받은 컬럼을 String 타입으로 Mybatis가 인지하여 String으로 select 할 수 있다.
