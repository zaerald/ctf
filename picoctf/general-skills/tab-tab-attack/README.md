# Tab, Tab, Attack

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip

## Extract zip file

```
unzip Addadshashanammu.zip

Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
```

## List files

```
ls -la

total 12K
drwxr-xr-x 1 zaerald zaerald   90 Jul  9 04:00 .
drwxr-xr-x 1 zaerald zaerald  232 Jul  9 03:59 ..
drwxr-xr-x 1 zaerald zaerald   28 Mar 16  2021 Addadshashanammu
-rw-r--r-- 1 zaerald zaerald 4.5K Jul  9 03:59 Addadshashanammu.zip
-rw-r--r-- 1 zaerald zaerald  932 Jul  9 04:00 README.md
```

## View Tree

```
tree Addadshashanammu

Addadshashanammu
└── Almurbalarammi
    └── Ashalmimilkala
        └── Assurnabitashpi
            └── Maelkashishi
                └── Onnissiralis
                    └── Ularradallaku
                        └── fang-of-haynekhtnamet

6 directories, 1 file
```

## Investigate file

```
cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku
ls -la fang-of-haynekhtnamet

-rwxr-xr-x 1 zaerald zaerald 8320 Mar 16  2021 fang-of-haynekhtnamet
```

## Execute File

```
./fang-of-haynekhtnamet

*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_f3553887}
```

## Flag

```
picoCTF{l3v3l_up!_t4k3_4_r35t!_f3553887}
```

