# Ex03 Django ORM Web Application
## Date:18/09/2024 

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![image](https://github.com/user-attachments/assets/bc0d5821-e363-4700-9ea8-dbe5e8f1dca3)


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
from .models import Bank,Loandetails

# Register your models here.
admin.site.register(Bank,Loandetails)

# Register your models here.
models.py
from django.db import models
from django.contrib import admin

class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    loan_period = models.CharField(max_length=10, default='12 months')  
    monthly_interest = models.DecimalField(max_digits=10, decimal_places=2)
    Submitted_documents = models.CharField(max_length=100, default='None')  

class Loandetails(admin.ModelAdmin):
    list_display = ('customer_id', 'customer_name', 'account_type', 'loan_amount', 'loan_period', 'monthly_interest', 'Submitted_documents')

```

## OUTPUT
![orm 2](https://github.com/user-attachments/assets/d2639ea4-2ab3-4cbb-bcd6-8d0e7199fc2f)

![orm 1](https://github.com/user-attachments/assets/f85404c1-e081-4fd6-aac7-15e0d6e49433)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
