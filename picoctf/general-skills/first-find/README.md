# First Find

Unzip this archive and find the file named 'uber-secret.txt'
Download zip file

## Unzip archive

```
unzip files.zip
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8
  inflating: files/satisfactory_books/23765.txt.utf-8
  inflating: files/satisfactory_books/16021.txt.utf-8
  inflating: files/13771.txt.utf-8
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
  inflating: files/adequate_books/more_books/1023.txt.utf-8
  inflating: files/adequate_books/46804-0.txt
  inflating: files/adequate_books/44578.txt.utf-8
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8
  inflating: files/acceptable_books/17880.txt.utf-8
  inflating: files/acceptable_books/17879.txt.utf-8
  inflating: files/14789.txt.utf-8
```

## View tree Overview

```
tree files
files
├── 13771.txt.utf-8
├── 14789.txt.utf-8
├── acceptable_books
│   ├── 17879.txt.utf-8
│   ├── 17880.txt.utf-8
│   └── more_books
│       └── 40723.txt.utf-8
├── adequate_books
│   ├── 44578.txt.utf-8
│   ├── 46804-0.txt
│   └── more_books
│       └── 1023.txt.utf-8
└── satisfactory_books
    ├── 16021.txt.utf-8
    ├── 23765.txt.utf-8
    └── more_books
        └── 37121.txt.utf-8

6 directories, 11 files
```

Viewing dir tree, helps me to gain understanding of the structure.

## Properly find file

```
find . -type f -name 'uber-secret.txt'

./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
```

## View file content

```
cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

picoCTF{f1nd_15_f457_ab443fd1}
```

## Flag

```
picoCTF{f1nd_15_f457_ab443fd1}
```

