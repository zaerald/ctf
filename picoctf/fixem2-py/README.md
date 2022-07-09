# fixme2.py

Fix the syntax error in the Python script to print the flag.
Download Python script

## Run the script

```
python3 fixme2.py
  File "/home/zaerald/workspace/github.com/zaerald/picoctf-journey/fixem2-py/fixme2.py", line 22
    if flag = "":
            ^
SyntaxError: invalid syntax
```

I have to fix line 22.

## Create a fixed version

```
cp fixme2.py fixed.py
```

## Fix error

```
diff -u fixme2.py fixed.py
```

```diff
--- fixme2.py
+++ fixed.py
@@ -19,7 +19,7 @@
 flag = str_xor(flag_enc, 'enkidu')

 # Check that flag is not empty
-if flag = "":
+if flag == "":
   print('String XOR encountered a problem, quitting.')
 else:
   print('That is correct! Here\'s your flag: ' + flag)
```

## Run fixed script

```
python3 fixed.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## Flag

```
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

