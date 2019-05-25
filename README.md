
# cbvlibrary

This is the code repository for tutorial [Class Based Views in Django](https://medium.com/all-about-django/class-based-views-in-django-89108c1f51fb)

It uses Class-Based Views to create CRUD interfaces for a `Book` model.

## Snaps

* ListView

![listview](.snaps/listview.png "ListView for Books")

* CreateView

![createview](.snaps/createview.png "CreateView of Book")

* DetailView

![detailview](.snaps/detailview.png "DetailView of Book")

* UpdateView

![updateview](.snaps/updateview.png "UpdateView of Book")

* DeleteView

![deleteview](.snaps/deleteview.png "DeleteView of Book")

## Setup Instructions

First make sure that you have the following installed.

* Python 3 and virtualenv

Now do the following to setup project

```
# assuming that the project is already cloned.

cd cbvlibrary

# one time
virtualenv -p $(which python3) pyenv

source pyenv/bin/activate

# one time or whenever any new package is added.
pip install -r requirements/dev.txt

# update settings
cp src/cbvlibrary/settings/local.sample.env src/cbvlibrary/settings/local.env

# generate a secret key or skip(has a default value) and then replace the value of `SECRET_KEY` in environment file(here local.env)
./scripts/generate_secret_key.sh

# update relevant variables in environment file

# run migrate
cd src
python manage.py migrate
```

To access webserver, run the following command

```
cd src
python manage.py runserver
```
