# Ex02 Django ORM Web Application
## Date:29/05/2025

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![image](https://github.com/user-attachments/assets/6746f882-8000-4fc6-91b2-708ae32f8109)

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
~~~
admin.py

from django.contrib import admin
from .models import Book
class BookAdmin(admin.ModelAdmin):
    list_display = ('book_id', 'title', 'author', 'genre', 'published_year', 'rating')
admin.site.register(Book, BookAdmin)

models.py

from django.db import models
class Book(models.Model):
    book_id = models.AutoField(primary_key=True)
    title = models.CharField(max_length=200)
    author = models.CharField(max_length=100)
    genre = models.CharField(max_length=50)
    published_year = models.IntegerField()
    rating = models.FloatField()

    def __str__(self):
        return self.title

~~~



## OUTPUT

Include the screenshot of your admin page.
![image](https://github.com/user-attachments/assets/4f824940-755a-4f37-a5e4-378b20d06f68)



## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
