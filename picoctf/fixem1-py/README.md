# fixme1.py

Fix the syntax error in this Python script to print the flag.
Download Python script

## Run python script

```
python3 fixme1.py
  File "/home/zaerald/workspace/github.com/zaerald/picoctf-journey/fixem1-py/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
```

Looks like I have to fix the script on line 20.

## Create a fixed version

```
cp fixme1.py fixed.py
```

## Fix error

```
diff -u fixme1.py fixed.py
```

```diff
--- fixme1.py
+++ fixed.py
@@ -17,5 +17,5 @@


 flag = str_xor(flag_enc, 'enkidu')
-  print('That is correct! Here\'s your flag: ' + flag)
+print('That is correct! Here\'s your flag: ' + flag)
```

## Run fixed script

```
python3 fixed.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
```

## Flag

```
picoCTF{1nd3nt1ty_cr1515_09ee727a}
```

