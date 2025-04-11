# Ex02 Django ORM Web Application
## Date: 11-04-2025

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).
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
from .models import Student,StudentAdmin,Employee,EmployeeAdmin
admin.site.register(Student,StudentAdmin)
admin.site.register(Employee,EmployeeAdmin)

models.py
from django.db import models
from django.contrib import admin

class Student(models.Model):
    referencenumber=models.CharField(max_length=20,help_text="refernce number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    phonenumber=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','phonenumber')

class Employee (models.Model):
    emp_id=models.CharField(primary_key=True,max_length=4,help_text='Employee ID')
    ename=models.CharField(max_length=50)
    post=models.CharField(max_length=20)
    salary=models.IntegerField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','salary')
```



## OUTPUT

![Screenshot 2025-04-11 184153](https://github.com/user-attachments/assets/1817b0ce-6727-4540-84c7-f18dfc2f1044)



## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
