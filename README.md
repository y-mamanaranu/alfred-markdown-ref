# Markdown REF
Modify link referance in markdown.

## Basic Usage
Modify link referance in markdown.
With HotKey, convert selection and paste modified version.
With Keyword, convert clipboard and paste modified version.
Plese note that all of square brackets `[]` with length of contenxt text is less than 4 is recognized as ref.
- `[A]`, `[11]`,`[A12]`: ref
- `[AAAA]`, `[AA12]`, `[https://bra.bra]`: not ref

```input.md
This is sample[B] of this workflow[1].
Some links[A] nomatter character[5].
You don' have to spesicfy ref links[D].
It skipps the corresponding number[C].
This[AAAA] will be ignored.
![alt text also need sufficient legth](https://imag.url)

[5]: some url1
[1]: some url2
[A]: some url3
[B]: some url4
[C]: some url5
```

``` modified.md
This is sample[1] of this workflow[2].
Some links[3] nomatter character[4].
You don' have to spesicfy ref links[5].
It skipps the corresponding number[6].
This[AAAA] will be ignored.
![alt text also need sufficient legth](https://imag.url)

[1]: some url4
[2]: some url2
[3]: some url3
[4]: some url1
[6]: some url5
```

## Spesify start number
With Keyword, you can spesify start number (>0).
e.g. `mdref 3`.

```modified-with-3.md
This is sample[3] of this workflow[4].
Some links[5] nomatter character[6].
You don' have to spesicfy ref links[7].
It skipps the corresponding number[8].
This[AAAA] will be ignored.
![alt text also need sufficient legth](https://imag.url)

[3]: some url4
[4]: some url2
[5]: some url3
[6]: some url1
[8]: some url5
```
