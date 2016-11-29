---
layout: post
title: "表单验证"
date: 2016-03-19 12:36:06 +0800
description: "tui framework 表单验证"
---

表单验证实例
{% highlight javascript %}
	t("#form_validate").validate({
		"rules": {
			"username": {require: {message: "请输入姓名"}, length: {max: 10, min: 3, message: "长度必须小于10大于1；"}},
			"gender": {require: {message: "请输选择性别"}},
			"remark": {require: {message: "请输入备注"}},
			"phone": {phone: {message: "手机号不合法"}},
			"cd": {cd: {message: "身份证不合法"}},
			"number": {type: {type: "number", message: "不是整数"}},
			"float": {type: {type: "float", message: "不是小数"}},
		},
		"onerror": function(error){
			alert(error.join(";"));
		}
	});
{% endhighlight %}

调用form方法`.validate(params)`来实现对表单的验证。
params参数说明，params总共由3个对象组成：rules，onerror，onsuccess。rules为验证规则、其他两个是成功和失败的事件。rules中的每一个对象都是form表单元素的name属性值。
`rules`中验证说明
======
<table class="table table-bordered table-responsive">
    <thead>
        <tr>
            <th>参数名称</th>
            <th>类型</th>
            <th>默认</th>
            <th>描述</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>require</td>
            <td>json</td>
            <td></td>
            <td>不能为空。</td>
        </tr>
        <tr>
            <td>length</td>
            <td>json</td>
            <td></td>
            <td>长度，其中包括`max`最大长度和`min`最小长度。</td>
        </tr>
        <tr>
            <td>phone</td>
            <td>json</td>
            <td></td>
            <td>验证手机号。</td>
        </tr>
        <tr>
            <td>cd</td>
            <td>json</td>
            <td></td>
            <td>验证身份证号</td>
        </tr>
        <tr>
            <td>type</td>
            <td>json</td>
            <td></td>
            <td>验证类型，其中type类型包括：`number`整数型,`+number`正整数型,`-number`负整数型,`float`浮点型,`+float`正浮点型,`-float`负浮点型,`decimal`金钱类型</td>
        </tr>
        <tr>
            <td>regex</td>
            <td>Regexp</td>
            <td></td>
            <td>正则表达式验证，regex为正则表达式例如：/^-[0-9]*[1-9][0-9]*$/</td>
        </tr>
        <tr>
            <td>message</td>
            <td>string</td>
            <td></td>
            <td>为错误提示信息！`通用`</td>
        </tr>
    </tbody>
</table>

事件
====
<table class="table table-bordered table-responsive">
    <thead>
        <tr>
            <th>事件名称</th>
            <th>事件参数</th>
            <th>事件描述</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>onerror</td>
            <td>message：错误信息数组</td>
            <td>当验证失败时触发。</td>
        </tr>
        <tr>
            <td>onsuccess</td>
            <td></td>
            <td>当验证成功时触发。</td>
        </tr>
    </tbody>
</table>
