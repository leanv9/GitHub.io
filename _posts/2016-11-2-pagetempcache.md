---
layout: post
title: "页面临时缓存"
date: 2016-11-2 10:05:05 +0800
description: "tui framework 页面缓存"
---

页面临时缓存
=====
页面临时缓存和缓存不同在于，页面临时缓存完全存储在内存中。但不是持久化保存，是通过手动设置和执行缓存。注意页面临时缓存使用一次后自动清空。
`1.设置`：通过`t.pageTempCache.set`来设置或更新页面缓存。
{% highlight javascript %}
	function pageOnJump(){
		t.pageTempCache.set();//当页面跳转前设置临时缓存当前页面。
	}
{% endhighlight %}


`2.缓存渲染`：通过`t.pageTempCache.get(fn)`，把当前已经缓存的当前页面渲染到当前位置，参数`fn`为当缓存渲染完毕后触发事件。
{% highlight javascript %}
	t.pageTempCache.get(function(){
		setvalue();
	});
{% endhighlight %}