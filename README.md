# Handy Code Snippets
A bunch of code snippets that may help you ;)

## What is this?

Basically a repository with handy code snippets. Not only related to programming languages, but can also be related to frameworks, technologies, etc.

## Programming Languages

### Java

To centralize a JFrame in the middle of the screen use `this.setLocationRelativeTo(null);`.

### Python

Sort a list of dictionaries based on a key.

```python
# e.g.: [{'name': 'Boyhood', 'year': 2014}, {'name': 'Citizen Kane', 'year': 1941}, {'name': 'Mad Max: Fury Road', 'year': 2015}]
# sortedList(aList, 'year')

def sortedList(aList, aKey):
  return sorted(aList, key=lambda k: k[key])
```

It is also possible to sort by a key of a key.

```python
aList = [
  {
    'name': 'Boyhood',
    'release_date': {
        'day': 11,
        'month': 'July',
        'year': 2014
      },
  },
  {
     'name': 'Citizen Kane',
     'release_date': {
        'day': 5,
        'month': 'September',
        'year': 1941
      }
  }
]

sorted(aList, key=lambda k: k['release_date']['year'])
```

### R

Read a file `ALL.csv` and coverts all the names in the columns to comma-separated string.

```R
names <- readLines("ALL.csv")
listOfNames <- ""
for (i in names) { listOfNames <- paste(listOfNames, "," , i) }
listOfNames <- gsub(" ", "", listOfNames)
substr(listOfNames, 2, nchar(listOfNames))
```

## Frameworks

### Flask

Use HTTPS/SSL on your web application. Don't forget to `pip install flask_sslify`.

```python
from flask_sslify import SSLify

sslify = SSLify(app)
```

### node.js

Use HTTPS/SSL on your web application. Don't forget to `npm install express-force-https`.

```javascript
var secure = require('express-force-https');
var app = express();
app.use(secure);
```

## Technologies

### TravisCI

- `travis encrypt-file config.ini --all`

  Run this command to encrypt the file `config.ini` and add the reference to `.travis.yml`.

## Text Editors

### vim

Notable commands:

- `:q` to close the file. Use `!` to force quit.
- `:w` to save your file.
- `/<word>` to search for a `<word>`, if you want to keep searching, type `/`.
- `dd` to delete a line.
- `i` to enter INSERT mode.
- `esc` to leave the INSERT mode.
- `v` to select the text (or `V` to select the whole line).
- `d` to cut, `y` to copy and `P` to paste.


## Operating Systems

### Linux

- Check your systems specs on your Terminal: `lshw` Use `--short` to show a short version.

### Unix
These commands are valid for Linux and macOS.

- `tail -f foo.log` to keep the file opened and showing the last updates on your file. Very useful for system logs.
- `touch` to create a new file.
- `mkdir` to create a new directory.
- `pwd` to show the current path.
- `whoami` to show the current logged user.
