# Magikarp Ground Mission

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `481e7b14`

## Launch an Instance

Endpoint

```
ssh ctf-player@venus.picoctf.net -p 52280
```

## List Files

```
ctf-player@pico-chall$ ls -la
total 16
drwxr-xr-x 1 ctf-player ctf-player 4096 Mar 16  2021 .
drwxr-xr-x 1 ctf-player ctf-player 4096 Jul  8 20:06 ..
-rw-r--r-- 1 ctf-player ctf-player   14 Mar 16  2021 1of3.flag.txt
-rw-r--r-- 1 ctf-player ctf-player   56 Mar 16  2021 instructions-to-2of3.txt
```

## Read Files

```
ctf-player@pico-chall$ cat 1of3.flag.txt instructions-to-2of3.txt
picoCTF{xxsh_
Next, go to the root of all things, more succinctly `/`
```

## Navigate to root and read interesting files

```
cd /
cat 2of3.flag.txt instructions-to-3of3.txt

0ut_0f_\/\/4t3r_
Lastly, ctf-player, go home... more succinctly `~`
```

## Navigate to home directory and read interesting files

```
cd ~
cat 3of3.flag.txt

1118a9a4}
```

## Concatenate files

```
cat ~/drop-in/1of3.flag.txt /2of3.flag.txt ~/3of3.flag.txt | tr -d '\n'

ctf-player@pico-chall$ cat ~/drop-in/1of3.flag.txt /2of3.flag.txt ~/3of3.flag.txt | tr -d '\n'
picoCTF{xxsh_0ut_0f_\/\/4t3r_1118a9a4}
```

## Flag

```
picoCTF{xxsh_0ut_0f_\/\/4t3r_1118a9a4}
```

