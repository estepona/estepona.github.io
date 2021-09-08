---
title: "a poem in machine code"
date: 2019-01-27
categories: dev

classes:
  - wide
---

I write poems. I wrote this short poem in 2015.

>梦
>
>我养了两只猫  
>一只叫冈仁波齐  
>一只叫南迦巴瓦  
>一只叫神山  
>一只叫山神  

Code is art. I wonder how it looks like in a computer's "eyes".

First, encode each character with [utf-8](https://en.wikipedia.org/wiki/UTF-8) into hex value. In Python, you get value like "\xe6\xa2\xa6" after `.encode('utf-8')`, "\x" is a way for Python to identify that is's a hex value, then `.hex()` removes all "\x"s:
```python
hex_val = c.encode('utf-8').hex()
```

Then the poem in utf-8 hex value looks like:
```
e6a2a6

e68891 e585bb e4ba86 e4b8a4 e58faa e78cab
e4b880 e58faa e58fab e58688 e4bb81 e6b3a2 e9bd90
e4b880 e58faa e58fab e58d97 e8bfa6 e5b7b4 e793a6
e4b880 e58faa e58fab e7a59e e5b1b1
e4b880 e58faa e58fab e5b1b1 e7a59e
```

It seems that in utf-8, each Chinese character in the poem is represented by 3 bytes. Separating each byte makes it look better. I really like this version, but it's harder to know which character they belong to.
```
e6 a2 a6

e6 88 91 e5 85 bb e4 ba 86 e4 b8 a4 e5 8f aa e7 8c ab
e4 b8 80 e5 8f aa e5 8f ab e5 86 88 e4 bb 81 e6 b3 a2 e9 bd 90
e4 b8 80 e5 8f aa e5 8f ab e5 8d 97 e8 bf a6 e5 b7 b4 e7 93 a6
e4 b8 80 e5 8f aa e5 8f ab e7 a5 9e e5 b1 b1
e4 b8 80 e5 8f aa e5 8f ab e5 b1 b1 e7 a5 9e
```

Further down the path, convert the hex values into machine code, 0 and 1:
```python
bin_val = bin(int(hex_val, 16))
```

Result:
```
111001101010001010100110

111001101000100010010001 111001011000010110111011 111001001011101010000110 111001001011100010100100 111001011000111110101010 111001111000110010101011
111001001011100010000000 111001011000111110101010 111001011000111110101011 111001011000011010001000 111001001011101110000001 111001101011001110100010 111010011011110110010000
111001001011100010000000 111001011000111110101010 111001011000111110101011 111001011000110110010111 111010001011111110100110 111001011011011110110100 111001111001001110100110
111001001011100010000000 111001011000111110101010 111001011000111110101011 111001111010010110011110 111001011011000110110001
111001001011100010000000 111001011000111110101010 111001011000111110101011 111001011011000110110001 111001111010010110011110
```

It is clear to see how utf-8 works, pretty amazing, right?

Again, separate each byte:
```
11100110 10100010 10100110

11100110 10001000 10010001 11100101 10000101 10111011 11100100 10111010 10000110 11100100 10111000 10100100 11100101 10001111 10101010 11100111 10001100 10101011
11100100 10111000 10000000 11100101 10001111 10101010 11100101 10001111 10101011 11100101 10000110 10001000 11100100 10111011 10000001 11100110 10110011 10100010 11101001 10111101 10010000
11100100 10111000 10000000 11100101 10001111 10101010 11100101 10001111 10101011 11100101 10001101 10010111 11101000 10111111 10100110 11100101 10110111 10110100 11100111 10010011 10100110
11100100 10111000 10000000 11100101 10001111 10101010 11100101 10001111 10101011 11100111 10100101 10011110 11100101 10110001 10110001
11100100 10111000 10000000 11100101 10001111 10101010 11100101 10001111 10101011 11100101 10110001 10110001 11100111 10100101 10011110
```

Now, there is really no way I can tell what they represent, that I wrote it, and that after I post it to the Internet this is what's actually stored! I do think it's beautiful. And so I heard that researchers and software engineers in the early days actually do things this way. What a time.

I also tried to encode it with encodings other than utf-8. For Chinese characters, it is in fact more efficient to use encodings like [gb2313](https://en.wikipedia.org/wiki/GB_2312), which uses only 2 bytes for each character, saving 1/3 more space compared to utf-8. But for the purpose of this post, you get the idea.
