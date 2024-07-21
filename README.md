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


Display all:
```
Notes.objectss.all()
```

Create new note:
```
new_note = Notes.objects.create(title="A second note", text="This is a second note")
```

Filter the notes and find the one where the "title" starts with:
```
Notes.objects.filter(title__startswith="My")
```

Filter the notes and find one that contains the word "Django" in the text:
```
Notes.objects.filter(text__icontains='Django')
```

Exclude a word from the search:
```
Notes.objects.exclude(text__icontains="Django")
```

Filter and exclude at the same time:
```
Notes.objects.filter(text__icontains="Django").exclude(title__icontains="Django")
```

Filter and exclude at the same time:
```
Notes.objects.filter(text__icontains="Django").exclude(title__icontains="Django")
```
