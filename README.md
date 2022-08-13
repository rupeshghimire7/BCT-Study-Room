
# StudyBCT - Find your study partner in WRC!

This is a web application for WRC that helps students to create their own chat rooms and communicate with every participant.

## Authors

- [Rupesh Ghimire](https://www.github.com/rupeshghimire7)
- [SandeshGC](https://www.github.com/SandeshGC)
- [Samir Gurung](https://www.github.com/Pikasam114)
- [Sailesh Ghimire](https://www.github.com/saileshghimire)



## 🚀 About Us
Rupesh Ghimire - Backend Developer  
Sandesh GC - Frontend Developer  
Samir Gurung - Frontend Developer  
Sailesh Ghimire - Backend Developer


## Roadmap
- Install django framework (Prerequisite Python3)
```
pip install Django
django-admin startproject PROJECT_NAME
```
After you go into the created directory, run:
```python
python manage.py runserver #it gets your server started
```

There are few basic files like urls.py, settings.py etc created which will be used soon.

- Create an app. Run:
```
python manage.py startapp APP_NAME
```
*Settings.py*
```
INSTALLED_APPS = [...,
                  "APP_NAME",
                  .....  ]
```
## <APP.PNG>

- In *urls.py* of project, we include path to redirect it to necessary paths and mostly, to urls.py of the app
*In Urls.py*
```
urlpattern= [
path("room/<str:id>", views.room, name='room')
]
```
*In Views.py*
```
def room(request, pk):
	return HttpResponse("Welcome to room")
    #return render(request, 'path-to-a-html-template')
```
When the url is changed to ....../room/1, it goes to room function in views.py and calls that function.
Which in this case responds with a page that says 'Welcome to room'.
Instead we can build a template and show by using *render* instead of *HttpResponse*

## Static Contents
Static: for static files in page : in template that uses static file : 
say index.html file:
			
```
{% load static %}  #loads static dir (named as static)
#For using the static element/content, refrence (href) is passed as:

<a href="{% static 'path_to_static_file' %}"> LINK <\a>  
``` 

## For Template Inheritance
- For including certain template
```
{% include 'path-to-the-template' %}
```
- Extending a parent template
```
{% extends 'path-to-parent-template' %}
```
- For using the varying code blocks of parent template in child template
```
{% block content %} *Your_code_here* {% endblock %}
```
- For conditions and python syntax. PS: it is similar for 'if conditions'   
    (item is Django's template variable)
    (item_list is a python list variable)
```
{% for item in item_list %} {{item}} {% endfor %}
```



### 💻 User-Interface of SERVER
