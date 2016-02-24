Revisions listed here will introduce a backwards incompatible change in the data model.  If you don't have any production data in django-crm (formerly minibooks) you can ignore these instructions and simply drop and recreate your database.

# [r11](https://code.google.com/p/django-crm/source/detail?r=11) #

To successfully upgrade past [r11](https://code.google.com/p/django-crm/source/detail?r=11), you need to complete the following steps:

  1. svn up -[r11](https://code.google.com/p/django-crm/source/detail?r=11)
  1. ./manage.py syncdb
  1. ./manage.py dbshell < apps/external\_apps/crm/migrations/001\_locations.sql
  1. ./manage.py migrate\_crm\_data
  1. svn up

[r11](https://code.google.com/p/django-crm/source/detail?r=11) is a "special" state of the code in which both models for storing address/phone info exist.  They will be removed in a future revision, making your old data inaccessible if you don't go through this step.  Please create a ticket if you have any questions.

# [r18](https://code.google.com/p/django-crm/source/detail?r=18) #

To successfully upgrade past [r18](https://code.google.com/p/django-crm/source/detail?r=18), you must first complete the [r11](https://code.google.com/p/django-crm/source/detail?r=11) upgrade (if need be) and then complete the following steps:

  1. svn up -[r18](https://code.google.com/p/django-crm/source/detail?r=18)
  1. ./manage.py syncdb
  1. ./manage.py migrate\_crm\_data
  1. ./manage.py dbshell < apps/external\_apps/crm/migrations/004\_business.sql

# [r21](https://code.google.com/p/django-crm/source/detail?r=21) #

  1. svn up -[r21](https://code.google.com/p/django-crm/source/detail?r=21)
  1. ./manage.py dbshell < apps/external\_apps/crm/migrations/005\_slug.sql
  1. ./manage.py migrate\_crm\_data
  1. ./manage.py dbshell < apps/external\_apps/crm/migrations/006\_slug\_not\_null.sql