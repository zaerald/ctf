# mus1c

I wrote you a song. Put it in the picoCTF{} flag format.

## Analyze the file

```
cat lyrics.txt

...
```

I don't understand what should I do here?
Are they a command?
Digging into this, it looks like the Rockstar programming language.

## Running the program

Output
```
114
114
114
111
99
107
110
114
110
48
49
49
51
114
Program completed in 67 ms
```

## Convert to ASCII characters

```
114 -> r
111 -> o
99  -> c
107 -> k
110 -> n
48  -> 0
49  -> 1
51  -> 3

rrrockn0113r
```

## Flag

```
picoCTF{rrrocknrn0113r}
```

