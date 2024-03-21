# Ex02 Django ORM Web Application
## Date:07-03-2024 

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).





## Entity Relationship Diagram
![314384626-6dd3589b-0e65-4495-b9e8-88b909a2de97](https://github.com/syedfayaz3105/ORM/assets/147144126/c38000cc-6a53-4c63-9ec5-514fadb0bb6d)



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

```
admin.py

from django.contrib import admin
from .models import Book,BookAdmin
admin.site.register(Book,BookAdmin)

models.py

from django.db import models
from django.contrib import admin
class Book(models.Model):
    book_id=models.IntegerField(primary_key=True)
    book_name=models.CharField(max_length=50)
    publisher_name=models.CharField(max_length=50)
    author_name=models.CharField(max_length=50)
    publisher_year=models.IntegerField()

class BookAdmin(admin.ModelAdmin):
    list_display=('book_id','book_name','publisher_name','publisher_year','author_name')

```

## OUTPUT

![314385491-df3dc118-40e6-46f1-b895-23524f55a9fc](https://github.com/syedfayaz3105/ORM/assets/147144126/0c7270b6-482f-45ff-8627-e9819f0aabaa)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
