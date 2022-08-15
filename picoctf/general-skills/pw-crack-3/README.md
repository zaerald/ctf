# PW Crack 3

Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag and the hash in the same directory too.
There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Examine script

```
cat level3.py

...
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
...
```
It requires a proper hashed password from the user.


There's a clue:
```python
# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
```

## Modify script

```
cp level3.py level3_modified.py
diff -u level3.py level3_modified.py
```

```diff
--- level3.py
+++ level3_modified.py
@@ -23,11 +23,11 @@
     return m.digest()


-def level_3_pw_check():
-    user_pw = input("Please enter correct password for flag: ")
+def level_3_pw_check(user_pw):
     user_pw_hash = hash_pw(user_pw)

     if( user_pw_hash == correct_pw_hash ):
+        print("Correct password:", user_pw)
         print("Welcome back... your flag, user:")
         decryption = str_xor(flag_enc.decode(), user_pw)
         print(decryption)
@@ -36,10 +36,12 @@


-level_3_pw_check()

 # The strings below are 7 possibilities for the correct password.
 #   (Only 1 is correct)
 pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

+for user_pw in pos_pw_list:
+    level_3_pw_check(user_pw)
+
```

## Run Script

```
python3 level3_modified.py

That password is incorrect
That password is incorrect
That password is incorrect
Correct password: dba8
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
That password is incorrect
That password is incorrect
That password is incorrect
```

```
python3 level3_modified.py | grep picoCTF

picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

## Flag

```
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

