# Ex02 Django ORM Web Application
## Date: 06/03/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![alt text](<WhatsApp Image 2024-03-07 at 22.40.45_a7b04a5b.jpg>)

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
MODELS.PY
from django.db import models
from django.contrib import admin
class Book(models.Model):
    bookno=models.IntegerField(primary_key="bookno")
    bookname=models.CharField(max_length=20)
    authorname=models.CharField(max_length=40)
    publishdate=models.DateField()
    price=models.IntegerField()
class BookAdmin(admin.ModelAdmin):
    list_display=("bookno", "bookname", "authorname", "publishdate","price");

    ADMIN.PY

    from django.contrib import admin
from .models import Book,BookAdmin
admin.site.register(Book,BookAdmin)
```


## OUTPUT

![alt text](<Screenshot 2024-03-07 220005.png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
