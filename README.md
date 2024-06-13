# Django-notes

# Django shell for creating and querying data

python manage.py shell
```
from notes.models import Notes
my_note = Notes.bojects.get(pk='1')
```

Can access the attributes like this:
```
my_note.title
my_note.text
```

Display all
```
Notes.objectss.all()
```
