# Ex02 Django ORM Web Application
## Date: 26.03.2025

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



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
## Models
``````````
from django.db import models
from django.contrib import admin
class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

    def __str__(self):
        return self.customer_name  # Optional, for better representation in admin or shell

class BankAdmin(admin.ModelAdmin):
    list_display = ('customer_id', 'customer_name', 'account_type', 'loan_amount', 'monthly_interest', 'due_date')
admin.site.register(Bank, BankAdmin)

```````````
## Admin
`````
from django.contrib import admin
from .models import Bank, Loandetails

admin.site.register(Bank)
admin.site.register(Loandetails)
``````
## OUTPUT
![image](https://github.com/user-attachments/assets/1bd6cf8f-df06-453a-9f0c-cbc28a97326d)

![image](https://github.com/user-attachments/assets/cf8df27c-e707-4907-ba51-69caa78a6f4d)


## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
