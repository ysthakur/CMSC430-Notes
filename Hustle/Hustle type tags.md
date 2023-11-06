---
tags:
  - type-tag
lang: hustle
---
We know that pointers in both the stack and heap will always be 8-byte/64-bit aligned,
meaning they end in `000` in binary.

- So now, immediate values (everything except `cons` and `box`) will use `000` for the 3 least significant bits
  - The bits to the left of that will determine whether it's an int, boolean, etc., just like before
  - Now only have 60 bits left for integers
    - 3 bits used for immediate tag (`000`)
    - 1 bit used for type tag
- `box`es will have `001` for their least significant bits
- `cons` will have `010` for their least significant bits

> [!WARNING]
> The last 3 bits for `cons` and `box` will have to be zeroed out before using them as pointers.