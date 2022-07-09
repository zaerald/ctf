# Wave a flag

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

## Check file type

```
file warm

warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=b11c22752c901adc13ba1ce86eda9d5516f22763, with debug_info, not stripped
```

## Make file executable

```
chmod u+x warm
ls -la warm

-rwxr--r-- 1 zaerald zaerald 11K Jul  9 03:36 warm
```

## Execute file

```
./warm
Hello user! Pass me a -h to learn what I can do!

./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
```

## Flag
```
picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
```

