# Static ain't always noise

Can you look at the data in this binary: static? This BASH script might help!

## Check `static` file type

```
file static

static: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=639391a8b15c579d69659462d3c935fa61693f17, not stripped
```
It's an executable file.

## Skim `ltdis.sh` Script

Usage is: `ltdis.sh <program-file>`

## Make script executable

```
chmod u+x ltdis.sh
ls -la ltdis.sh

-rwxr--r-- 1 zaerald zaerald 785 Jul  9 03:51 ltdis.sh
```

## TRY file execution

```
./ltdis.sh static

Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
```

## List new files

```
ls -la

total 32K
drwxr-xr-x 1 zaerald zaerald  140 Jul  9 03:54 .
drwxr-xr-x 1 zaerald zaerald  204 Jul  9 03:51 ..
-rwxr--r-- 1 zaerald zaerald  785 Jul  9 03:51 ltdis.sh
-rw-r--r-- 1 zaerald zaerald  644 Jul  9 03:54 README.md
-rw-r--r-- 1 zaerald zaerald 8.2K Jul  9 03:51 static
-rw-r--r-- 1 zaerald zaerald 1.7K Jul  9 03:54 static.ltdis.strings.txt
-rw-r--r-- 1 zaerald zaerald 6.4K Jul  9 03:54 static.ltdis.x86_64.txt
```

## Preview files

```
less static.ltdis.strings.txt static.ltdis.x86_64.txt
```

Looking at this does not make sense to me.

## TRY grep for flags

```
cat static.ltdis.strings.txt static.ltdis.x86_64.txt | grep picoCTF

   1020 picoCTF{d15a5m_t34s3r_98d35619}
```

## Flag

```
picoCTF{d15a5m_t34s3r_98d35619}
```

