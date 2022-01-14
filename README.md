# web_middle  
110710527王博緯  
[參考網站](https://code.ziqiangxuetang.com/django/django-basic.html)

Django將架構分成三部分
Model : 定義資料庫的東西 ( ORM )，這層通常是直接和資料有關。  
  
Template : 最終呈現給客戶端的畫面。  

View : 中間層，負責 Model 和 Template 之間的業務邏輯。  
  
# django練習  

先下載好python  
安裝django  
>pip install django

開啟一個django project  

>django-admin startproject middle

然後在終端執行  
```
python manage.py runserver
```
就可以看到執行成功的畫面了  
![image](https://github.com/sleepy9487/web_middle/blob/master/images/1.JPG)  

## 建立app(功能)
之後我們要創建app(功能)  
終端輸入  
>python manage.py startapp food
![image](https://github.com/sleepy9487/web_middle/blob/master/images/2.JPG)  
請在 settings.py 裡面的 **INSTALLED_APPS** 加入 food (新建立的 App 名稱)  
![image](https://github.com/sleepy9487/web_middle/blob/master/images/3.JPG)  
  
## views&templates  
在 templates 裡面新增一個  **hello.html**  
並輸入程式碼:  
```  
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>title</title>
</head>
<body>
    {{test}}
</body>
</html>
```  
![image](https://github.com/sleepy9487/web_middle/blob/master/images/4.JPG)  
html裡的test就是要與views連動回傳的值  

###views  
在views底下輸入程式碼 : 
```python
from django.shortcuts import render


# Create your views here.
def hello_view(request):
    return render(request, 'hello.html', {
        'test': "Hello this is a test ",
    })

```  
>回傳test>Hello this is a test
![image](https://github.com/sleepy9487/web_middle/blob/master/images/5.JPG)
### urls  
最後我們要增添url  
將views與template的連動可以呈現出來  
![image](https://github.com/sleepy9487/web_middle/blob/master/images/6.JPG)  
>hello_views的函數

最後終端輸入python manage.py server後  
在原網址後添加/hello 就可以看到新增的網頁了~
![image](https://github.com/sleepy9487/web_middle/blob/master/images/7.JPG)





