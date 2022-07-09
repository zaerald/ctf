# PW Crack 1

Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag in the same directory too.

## Run the python script

```
python3 level1.py

Please enter correct password for flag:
```

It requires me to enter a password, that could be generated from `level1.flag.txt.enc`.

## Check file type

```
file level1.flag.txt.enc
level1.flag.txt.enc: data
```

## TRY to read the file

```
cat level1.flag.txt.enc
FPR
   umw
iK
_i
  UD%                                                                          
```

## Read the script

```
cat level1.py

...
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
...
```

There is a condition that checks for `691d` input, that will provide the flag.

## Run script and provide input

```
python3 level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
```

## Flag

```
picoCTF{545h_r1ng1ng_56891419}
```

