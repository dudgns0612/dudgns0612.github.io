---
layout: post
title: "[Jquery] children()과 find() 차이점"
excerpt: "Mybatis 사용 시 Mapper에서 변수명 자동 CamelCase변환 옵션주기."
categories: [Jquery]
date: 2017-06-24
modified: 2017-06-24
comments: true
---

children와 find의 기능은 자식을 검색 할 수 있도록 제공하는 함수이다.<br />
하지만 두 함수는 서로 미묘 하지만 큰 차이가 존재한다.<br />



### Code Blocks

​Mybatis 사용 시 Mapper에서 변수명 자동 CamelCase변환 옵션주기.<br />

{% highlight html %}
<div class="parent">
  <div class="child1">
      <div class="child2"></div>
  </div>
</div>
{% endhighlight %}

### Additional Description
이렇게 있을경우 $('.parent')를 셀렉터로 사용할 경우 children()으로는 직계 인 <br />
child1만 자식으로 조회 할 수 있고<br />
find는 직계 뿐만아니라 자손들 전부 검색이 가능하기 때문에 <br />
child2까지 셀렉트 할 수 있다.
