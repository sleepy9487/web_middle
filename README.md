# web_middle  
110710527王博緯  

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
![image]()  
