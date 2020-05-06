---
title: Numeral, Metric and Binary Prefixes
description: Uni, Bi, Kilo, Mibi etc.
author: ibraheem_rodrigues
category: mathematics
---

{% include toc.md %}

## Small Quantity Prefixes


|    Quantity     | Common Prefixes       | IUPAC Standard (Chemical Names)[^chemical] |
|:---------------:|-----------------------|--------------------------------------------|
| $$\frac{1}{2}$$ | Semi-, Demi-, Hemi-   | N/A                                        |
|        1        | Uni-, Mono-           | Mono-, [hen-](#iupac-names-)                |
|        2        | Bi-, Di-              | Di-, [do-](#iupac-names-)                                         |
|        3        | Tri-                  | Tri                                        |
|        4        | Quad-, Tetra-         | Tetra-                                     |
|        5        | Penta-                | Penta-                                     |
|        6        | Sex-, Hex-            | Hexa-                                      |
|        7        | Sept-, Hept-          | Hepta-                                     |
|        8        | Oct-                  | Octa-                                      |
|        9        | Nov-, Non-            | Nona-                                      |
|       10        | Dec-                  | Deca-                                      |
|       11        | Undec-, Hendec-       |                                            |
|       12        | Duodec-, Dodec-       |                                            |
|       13        | Tredec-, Tridec-      |                                            |
|       20        | Icosa-                | Icosa-                                     |
|       100       | Centi-, Hecta-        | Hecta-                                     |
|      1000       | Kilo-,                | Kilia-                                     |
|       Few       | Pauci-, Oligo-        | N/A,  Oligo- sometimes used                |
|      Many       | Multi-, Pluri-, Poly- | N/A, Poly- sometimes used                  |
|       All       | Omni-                 | N/A                                        |

### IUPAC Names [^chemical]

For higher numtiples of 10, 100 and 1000:
- 30, 40, 50 etc: Add **-conta-** (tetraconta-, pentaconta-)
- 300, 400, 500 etc: Add **-cta-** (tricta-, tetracta-)
- 2000, 3000 etc: Add **-lia-** (hexalia-, hexalia-)

To build numbers, join prefixes for each digit (replace mono- with **hen-** and di- with **do-**)

$$
\begin{align}
421 = & 1 + 20 + 400 \\
\rightarrow &\text{ hen-, icosa-, tetracta-} \\
= & \text{ henicosatetracta-}
\end{align}
$$

For complex features, **-kis-** is added:

- 5 = **penta*kis*-**
- 421 = **henicosatetracta*kis*-**
- Note **mono-** remains unchanged, di- becomes **bis-** and tri- becomes **tris-**

[^chemical]: [https://www.qmul.ac.uk/sbcs/iupac/misc/numb.html](https://www.qmul.ac.uk/sbcs/iupac/misc/numb.html) Accessed 1/05/2020

## Metric and Binary Prefixes

| Metric Prefix[^metric] | Symbol | Factor        | Factor         | Symbol | Metric Prefix |
|------------------------|--------|---------------|----------------|--------|---------------|
| Yotta                  | Y      | $$ 10^{24} $$ | $$ 10^{-24} $$ | y      | Yocto         |
| Zetta                  | Z      | $$ 10^{21} $$ | $$ 10^{-21} $$ | z      | Zepto         |
| Exa                    | E      | $$ 10^{18} $$ | $$ 10^{-18} $$ | a      | Atto          |
| Peta                   | P      | $$ 10^{15} $$ | $$ 10^{-15} $$ | f      | Femto         |
| Tera                   | T      | $$ 10^{12} $$ | $$ 10^{-12} $$ | p      | Pico          |
| Giga                   | G      | $$ 10^{9} $$  | $$ 10^{-9} $$  | n      | Nano          |
| Mega                   | M      | $$ 10^{6} $$  | $$ 10^{-6} $$  | µ      | Micro         |
| Kilo                   | k      | $$ 10^{3} $$  | $$ 10^{-3} $$  | m      | Milli         |
| Hecto                  | h      | $$ 10^{2} $$  | $$ 10^{-2} $$  | c      | Centi         |
| Deca                   | da     | $$ 10^{1} $$  | $$ 10^{-1} $$  | d      | Deci          |

When used to denote a number of bits/bytes (kilobyte, megabit, etc.), there is some ambiguity as whether these units refer to a multiple of $$ 10^{3} = 1000 $$, as above, or a multiple of $$ 2^{10} = 1024 $$. The IEC defines the following **Binary Prefixes** in an attempt to alleviate this issue, although adoption is ultimately implementation dependent.

| Binary Prefix[^binary] | Symbol | Factor                             |
|------------------------|--------|------------------------------------|
| Yobi                   | Yi     | $$ 2^{80} $$                       |
| Zebi                   | Zi     | $$ 2^{70} $$                       |
| Exbi                   | Ei     | $$ 2^{60} = 1152921504606846976 $$ |
| Pebi                   | Pi     | $$ 2^{50} = 1125899906842624 $$    |
| Tebi                   | Ti     | $$ 2^{40} = 1099511627776 $$       |
| Gibi                   | Gi     | $$ 2^{30} = 1073741824 $$          |
| Mebi                   | Mi     | $$ 2^{20} = 1048576 $$             |
| Kibi                   | Ki     | $$ 2^{10} = 1024 $$                |


[^metric]: [https://physics.nist.gov/cuu/Units/prefixes.html](https://physics.nist.gov/cuu/Units/prefixes.html) Accessed 27/04/2020.
[^binary]: [https://physics.nist.gov/cuu/Units/binary.html](https://physics.nist.gov/cuu/Units/binary.html) Accessed 27/04/2020.
