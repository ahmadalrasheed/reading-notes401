## A Beginner's Guide to Docker
![docker](https://docs.docker.com/engine/images/architecture.svg)

### What is Docker?

Docker its a tool to isolate the whole development environment you are working on , programming language, software packages, databases, and more.

### Why Docker?

With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around.

## How It works ?
Docker is really just Linux containers which are a type of virtualization.
Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.


### Containers Vs Virtual Environment
Virtual environments are used to isolate Python software packages locally.But Docker is used to isolate the whole development environment.


## Library Website and API

### What is Django REST frameworks
Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

### How It works ?

first of all before we can use Django REST Framework , we must create a Django project like we took before in previous lab , and create website that hold information about specific model.

after that, Django REST Framework is added just like any other third-party app. Make sure to quit the local server Control + c if it is still running. Then on the command line type the below.


1. We have to install it: 

>`$ pipenv install djangorestframework~=3.11.0`

2. Then ,Add it to the installed apps in settings

>`INSTALLED_APPS`


3. Then ,Create you app to hold API info

>`python manage.py startapp api`

4. include the app in the projects URLs

>` path('', include('books.urls')), # new`

5. add view to the API application 

>from rest_framework import generics
from books.models import Book
from .serializers import BookSerializer
class BookAPIView(generics.ListAPIView):
    queryset = Book.objects.all()
    serializer_class = BookSerializer


6. Then import it into URLS 


>from django.urls import path
from .views import BookAPIView
urlpatterns = [
    path('', BookAPIView.as_view()),
]

7. create serializer file in you API application

**Serializers: A serializer translates data into a format that is easy to consume over the internet, typically JSON**

>`touch api/serializers.py`


8. Then update the serializer



>from rest_framework import serializers
from books.models import Book
class BookSerializer(serializers.ModelSerializer):
    class Meta:
        model = Book
        fields = ('title', 'subtitle', 'author', 'isbn')


9. Navigate to `http://127.0.0.1:8000/api/`

**Then you will see:**

![](https://djangoforapis.com/assets/images/02_book_api.png)






