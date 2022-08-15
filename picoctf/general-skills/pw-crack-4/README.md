# PW Crack 4

Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag and the hash in the same directory too.
There are 100 potential passwords with only 1 being correct. You can find these by examining the password checker script.

## Examine script

```
cat level4.py

...
pos_pw_list = ["8c86", "7692", "a519", "3e61", "7dd6", "8919", "aaea", "f34b", "d9a2", "39f7", "626b", "dc78", "2a98", "7a85", "cd15", "80fa", "8571", "2f8a", "2ca6", "7e6b", "9c52", "7423", "a42c", "7da0", "95ab", "7de8", "6537", "ba1e", "4fd4", "20a0", "8a28", "2801", "2c9a", "4eb1", "22a5", "c07b", "1f39", "72bd", "97e9", "affc", "4e41", "d039", "5d30", "d13f", "c264", "c8be", "2221", "37ea", "ca5f", "fa6b", "5ada", "607a", "e469", "5681", "e0a4", "60aa", "d8f8", "8f35", "9474", "be73", "ef80", "ea43", "9f9e", "77d7", "d766", "55a0", "dc2d", "a970", "df5d", "e747", "dc69", "cc89", "e59a", "4f68", "14ff", "7928", "36b9", "eac6", "5c87", "da48", "5c1d", "9f63", "8b30", "5534", "2434", "4a82", "d72c", "9b6b", "73c5", "1bcf", "c739", "6c31", "e138", "9e77", "ace1", "2ede", "32e0", "3694", "fc92", "a7e2"]
```

Using the hint again.

## Modify script

```
cp level4.py level4_modified.py
diff -u level4.py level4_modified.py
```

```diff
--- level4.py
+++ level4_modified.py
@@ -23,20 +23,18 @@
     return m.digest()


-def level_4_pw_check():
-    user_pw = input("Please enter correct password for flag: ")
+def level_4_pw_check(user_pw):
     user_pw_hash = hash_pw(user_pw)

     if( user_pw_hash == correct_pw_hash ):
+        print("Correct password:", user_pw)
         print("Welcome back... your flag, user:")
         decryption = str_xor(flag_enc.decode(), user_pw)
         print(decryption)
         return
-    print("That password is incorrect")



-level_4_pw_check()



@@ -44,3 +42,5 @@
 #   (Only 1 is correct)
 pos_pw_list = ["8c86", "7692", "a519", "3e61", "7dd6", "8919", "aaea", "f34b", "d9a2", "39f7", "626b", "dc78", "2a98", "7a85", "cd15", "80fa", "8571", "2f8a", "2ca6", "7e6b", "9c52", "7423", "a42c", "7da0", "95ab", "7de8", "6537", "ba1e", "4fd4", "20a0", "8a28", "2801", "2c9a", "4eb1", "22a5", "c07b", "1f39", "72bd", "97e9", "affc", "4e41", "d039", "5d30", "d13f", "c264", "c8be", "2221", "37ea", "ca5f", "fa6b", "5ada", "607a", "e469", "5681", "e0a4", "60aa", "d8f8", "8f35", "9474", "be73", "ef80", "ea43", "9f9e", "77d7", "d766", "55a0", "dc2d", "a970", "df5d", "e747", "dc69", "cc89", "e59a", "4f68", "14ff", "7928", "36b9", "eac6", "5c87", "da48", "5c1d", "9f63", "8b30", "5534", "2434", "4a82", "d72c", "9b6b", "73c5", "1bcf", "c739", "6c31", "e138", "9e77", "ace1", "2ede", "32e0", "3694", "fc92", "a7e2"]

+for user_pw in pos_pw_list:
+  level_4_pw_check(user_pw)
```

## Run Script

```
python3 level4_modified.py

Correct password: 607a
Welcome back... your flag, user:
picoCTF{fl45h_5pr1ng1ng_d770d48c}
```

```
python3 level4_modified.py | grep picoCTF

picoCTF{fl45h_5pr1ng1ng_d770d48c}
```

## Flag

```
picoCTF{fl45h_5pr1ng1ng_d770d48c}
```

