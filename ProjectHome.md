# django-crm #

django-crm is an open source Django Customer Relationship Management (CRM) pluggable app.

This project was originally extracted from [minibooks](https://secure.caktusgroup.com/projects/minibooks/), the open source Django CRM and bookkeeping package.

## Quick Start ##
While it's just a Django app, the easiest way to get started with django-crm is to download the sample project in SVN:
```
svn checkout http://django-crm.googlecode.com/svn/trunk/sample_project sample_project
```

Configure your database settings and SECRET\_KEY in settings.py, run `./manage.py syncdb`, and `./manage.py runserver`.

## Dependencies ##
django-crm depends on the following pluggable apps:

  * [django-contactinfo](http://code.google.com/p/django-contactinfo/)
  * [django-countries](http://code.google.com/p/django-countries/)
  * [django-crumbs](http://code.google.com/p/django-crumbs/)
  * [django-notify](http://code.google.com/p/django-notify/)
  * [django-ajax-selects](http://code.google.com/p/django-ajax-selects/)
  * [django-pagination](http://code.google.com/p/django-pagination/)

If you're using [django-dependency](http://code.google.com/p/django-dependency/) in your project, your DEPENDENCIES should look something like this:

```
DEPENDENCIES = (
    deps.SVN(
        'http://django-crm.googlecode.com/svn/trunk/crm',
        root=DEPDENDENCY_ROOT,
    ),
    deps.SVN(
        'http://django-contactinfo.googlecode.com/svn/trunk/contactinfo',
        root=DEPDENDENCY_ROOT,
    ),
    deps.SVN(
        'http://django-countries.googlecode.com/svn/trunk/countries',
        root=DEPDENDENCY_ROOT,
    ),
    deps.SVN(
        'http://django-crumbs.googlecode.com/svn/trunk/crumbs',
        root=DEPDENDENCY_ROOT,
    ),
    deps.SVN(
        'http://django-notify.googlecode.com/svn/trunk/django_notify',
        root=DEPDENDENCY_ROOT,
    ),
    deps.SVN(
        'http://django-ajax-selects.googlecode.com/svn/trunk/ajax_select',
        root=DEPDENDENCY_ROOT,
    ),
    deps.SVN(
        'http://django-pagination.googlecode.com/svn/trunk/pagination',
        root=DEPDENDENCY_ROOT,
    ),
)
```

## Features ##
Users in an optional "Contact Notifications" Group will receive an email including a diff of the changes made.

## Sponsors ##
Django development by [Caktus Consulting Group, LLC](http://www.caktusgroup.com/services/).