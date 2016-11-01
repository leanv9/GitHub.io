---
layout: post
title: "actionsheet"
date: 2016-03-19 19:23:06 +0800
description: "tui framework actionsheet"
---

actionsheet
===

actionsheet方法：`t.popupAction(popup_id, function(obj){})`
参数1：要弹出的div的id。  
参数2：处理弹出后点击按钮的事件，其中`obj.action`为按钮的名称，用来判断用户点击了哪个按钮。
  
样式1  
<img src="/images/sheet1.png" width="300px">
{% highlight html %}
    <a id="action1" href="" class="btn bg_teal">action1</a>
            
    <div id="action-modal1" class="popup-action">
        <div class="action-title">
            <div class="center" style="width: 100%">tui framework</div>
        </div>
        <div class="action-btn middle modal-btn">alert</div>
        <div class="action-btn middle modal-btn">cancel</div>
        <div class="action-btn middle modal-btn">config</div>
    </div>
    
    <script>
        t("#action1").click(function(){
            t.popupAction("action-modal1");
            return false;
        });
    </script>
{% endhighlight %}
  
    
样式2  
<img src="/images/sheet2.png" width="300px">
{% highlight html %}
    <a id="action2" href="" class="btn bg_blue">action2</a>
            
    <div id="action-modal2" class="popup-action">
        <div class="action-title">
            <div class="blue title-btn action-btn middle">取消</div>
            <div class="center">tui framework</div>
            <div class="title-btn blue action-btn middle">完成</div>
        </div>
        <div class="action-content">
            <p>
                fdsajfdsafkjlsdalfkslafjdfdjaslkfd;safdlasjfdsafdsalkfdsafj;dsafjdls;afkdslafdasklf;dsjafjklsafjldsa;jfkldsa;fjdksla;fds123123</p>
            <p>
                fdsajfdsafkjlsdalfkslafjd
                fdjaslkfd;safdlasjfdsa
                fdsalkfdsafj;dsafjdls;afkdsla
                fdasklf;dsjafjklsafjldsa;
                jfkldsa;fjdksla;fds
            </p>
            <p>
                fdsajfdsafkjlsdalfkslafjd
                fdjaslkfd;safdlasjfdsa
                fdsalkfdsafj;dsafjdls;afkdsla
                fdasklf;dsjafjklsafjldsa;
                jfkldsa;fjdksla;fds
            </p>
        </div>
    </div>
    
    <script>
        t("#action2").click(function(){
            t.popupAction("action-modal2");
            return false;
        });
    </script>
{% endhighlight %}
  
样式3  
<img src="/images/sheet3.png" width="300px">
{% highlight html %}
    <a id="action3" href="" class="btn bg_cyan">action3</a>
    
    <div id="action-modal3" class="popup-action">
        <div class="action-title">
            <div class="blue title-btn action-btn middle">取消</div>
            <div class="center">tui framework</div>
            <div class="title-btn blue action-btn middle">完成</div>
        </div>
        <div class="action-select">
            <div class="select-item">
                <ul id="u1">
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                </ul>
            </div>
            <div class="select-item">
                <ul id="u2">
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                </ul>
            </div>
            <div class="select-item">
                <ul id="u3">
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                    <li>fdsafsa</li>
                </ul>
            </div>
        </div>
    </div>
    
    <script>
        t("#action3").click(function(){
            t.popupAction("action-modal3");
            return false;
        });
    </script>
{% endhighlight %}
  
样式4  
<img src="/images/sheet4.png" width="300px">
{% highlight html %}
    <a id="action4" href="" class="btn bg_cyan">透明</a>
    
    <div id="action-4" class="popup-action popup-action-op">
        <div class="action-btn middle modal-btn">alert</div>
        <div class="action-btn middle modal-btn">cancel</div>
        <div class="action-btn middle modal-btn">config</div>
    </div>
    
    <script>
        t("#action4").click(function(){
            t.popupAction("action-4");
            return false;
        });
    </script>
{% endhighlight %}