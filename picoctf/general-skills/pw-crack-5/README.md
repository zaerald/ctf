# PW Crack 5

Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag and the hash in the same directory too. Here's a dictionary with all possible passwords based on the password conventions we've seen so far.

## Analyze script and dictionary

```
cat level5.py
cat dictionary.txt
```

It is the same from before but we are using the dictionary to run through the passwords.

## Modify script

```
cp level5.py level5_modified.py
diff -u level5.py level5_modified.py
```

```diff
--- level5.py
+++ level5_modified.py
@@ -23,18 +23,19 @@
     return m.digest()


-def level_5_pw_check():
-    user_pw = input("Please enter correct password for flag: ")
+def level_5_pw_check(user_pw):
     user_pw_hash = hash_pw(user_pw)

     if( user_pw_hash == correct_pw_hash ):
+        print("Correct password:", user_pw)
         print("Welcome back... your flag, user:")
         decryption = str_xor(flag_enc.decode(), user_pw)
         print(decryption)
         return
-    print("That password is incorrect")



-level_5_pw_check()
+passwords = open('dictionary.txt', 'r').read().splitlines()
+for dict_pw in passwords:
+  level_5_pw_check(dict_pw)
```

## Run Script

```
python3 level5_modified.py

Correct password: 9581
Welcome back... your flag, user:
picoCTF{h45h_sl1ng1ng_36e992a6}
```

```
python3 level5_modified.py | grep picoCTF

picoCTF{h45h_sl1ng1ng_36e992a6}
```

## Flag

```
picoCTF{h45h_sl1ng1ng_36e992a6}
```

