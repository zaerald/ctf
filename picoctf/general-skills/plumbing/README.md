# plumbing

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.


## Connect to the remote server

```
nc jupiter.challenges.picoctf.org 7480
```

It is a stream of text

## Grep the output

```
nc jupiter.challenges.picoctf.org 7480 | grep picoCTF

picoCTF{digital_plumb3r_06e9d954}
```

## Flag

```
picoCTF{digital_plumb3r_06e9d954}
```

