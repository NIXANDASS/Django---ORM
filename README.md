# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram



## DESIGN STEPS

### STEP 1:To create admin account enter the following command to create a superuser:
python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py createsuperuser

### STEP 2:Add the username and email for the superuser

### STEP 3:The next prompt in the shell is for your password. Add a strong password and press the Enter key to confirm it once again
superuser is created successfully.


## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

admin.py
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```



## OUTPUT

![Screenshot (35)](https://user-images.githubusercontent.com/118781418/213214625-a4001d5e-3136-451b-82c7-35b3f39b3c9d.png)

## RESULT
PROGRAM WAS EXECUTED SUCCESSFULLY
