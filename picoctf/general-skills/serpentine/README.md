# Serpentine

Find the flag in the Python script!
Download Python script


## Run script

```
python3 serpentine.py


    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
You can do it!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
```

## Modify script

```
cp serpentine.py serpentine_modified.py
diff -u serpentine.py serpentine_modified.py
```

```diff
--- serpentine.py
+++ serpentine_modified.py
@@ -66,7 +66,7 @@
       print_encouragement()

     elif choice == 'b':
-      print('\nOops! I must have misplaced the print_flag function! Check my source code!\n\n')
+      print_flag()

     elif choice == 'c':
       sys.exit(0)
```

## Run modified script

```
python3 serpentine_modified.py

...
Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c)
```

## Flag

```
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}
```

