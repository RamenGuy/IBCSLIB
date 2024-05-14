# Manual Binary Conversion Guide

Start by taking your number. For this example, we'll use **105**. 
Next, find the largest binary value (such as 1, 2, 4, 8, 16, and so on) that fits into the number. In this case, that value is **64**. So we write it like this:
```
-- -- -- - - - -
64 32 16 8 4 2 1
```
As 64 fits in, we set it to 1:
```
1  -- -- - - - -
64 32 16 8 4 2 1
```
Taking 64 away from 105, we get 41. From here, we get the next value that fits into that number. Here, that's **32**. So we set 32 to 1 as well:
```
1  1  -- - - - -
64 32 16 8 4 2 1
```
Take 32 away from 41 to get 9, which **8** fits into. We take the values between our last 1 and our next 1 and set them to 0 as follows:
```
1  1  0  1 - - -
64 32 16 8 4 2 1
```
Subtract 8 from 9 to get **1**, which allows us to cleanly finish: 
```
1  1  0  1 0 0 1
64 32 16 8 4 2 1
```
There's our answer - 1101001, the binary represantation of the denary number 105.

Now, the other direction - starting with a binary value and converting it to denary. We'll take 11011010.
```
1   1  0  1  1 0 1 0
128 64 32 16 8 4 2 1
```
It's a lot simpler - for each 1, add the corresponding values together.
```
2 + 8 + 16 + 64 + 128 = 218
```
So we end with 218. Just to check, let's convert that back into binary:
```
--- -- -- -- - - - -
128 64 32 16 8 4 2 1
```
218 - 128 = 90

90 - 64 = 26

26 - 16 = 10

10 - 8 = 2

2 - 2 = 0
```
1   1  0  1  1 0 1 0
128 64 32 16 8 4 2 1
```
11011010 = 11011010.
