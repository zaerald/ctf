# Glitch Cat

Our flag printing service has started glitching!
`$ nc saturn.picoctf.net 53933`

## Run the command

```
nc saturn.picoctf.net 53933

'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
```

The numbers that start with `0x` feels like a hexadecimal numbers. Let's try to convert them into letters.

```
chr(0x61) -> a
chr(0x34) -> 4
chr(0x33) -> 3
chr(0x39) -> 9
chr(0x32) -> 2
chr(0x64) -> d
chr(0x32) -> 2
chr(0x65) -> e
```

## Flag

```
picoCTF{gl17ch_m3_n07_a4392d2e}
```

