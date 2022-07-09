# Nice netcat...

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22342`, but it doesn't speak English...

## Execute command

```
nc mercury.picoctf.net 22342

112
105
99
111
67
84
70
123
103
48
48
100
95
107
49
116
116
121
33
95
110
49
99
51
95
107
49
116
116
121
33
95
53
102
98
53
101
53
49
100
125
10
```

I'm not sure what to do next. There should be something to decode this list of numbers. Are they ASCII code?

## TRY to convert numbers to ASCII.

Converting numbers to ASCII using this table: https://www.rapidtables.com/code/text/ascii-table.html

```
112 -> p
105 -> i
99  -> c
111 -> o
67  -> C
```

They are ASCII character code!

## Convert one code to a letter

```
echo 112 | awk '{ printf( "%c", $0 ); }'
```

## Automate Convert the code list to ASCII

```
nc mercury.picoctf.net 22342 | awk '{ printf( "%c", $0 ); }'

picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}
```

