# PW Crack 2

Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag in the same directory too.

## Read the script

```
cat level2.py

...
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) ):
        print("Welcome back... your flag, user:")
...
```

Checks for input `chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)`.

## Convert hex to letters

```
chr(0x34) -> 4
chr(0x65) -> e
chr(0x63) -> c
chr(0x39) -> 9
```

## Run script with input

```
python3 level2.py

Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```

## Flag

```
picoCTF{tr45h_51ng1ng_9701e681}
```

