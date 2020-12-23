# Computer Systems: A Programmer's Perspective, 3rd Edition (Global Edition)

I loved the 2nd edition of this book so much that I picked up the 3rd edition (which uses x86_64 instead of x86) when I was visiting India.
The authors Bryant and O'Hallaron maintain an [**errata list**](https://csapp.cs.cmu.edu/3e/errata.html) for the **North American edition** of this book.

The catch is that this North American edition errata list does not cover the errors in the Global edition of this book.
Here is the message from the authors:

> **Note on the Global Edition**: Unfortunately, the publisher arranged for the generation of a different set of practice and homework problems in the global edition.
The person doing this didn't do a very good job, and so these problems and their solutions have many errors.
We have not created an errata for this edition.

So, the publisher hired two people from India to modify the original US textbook's problems in the Global edition.
This is a typical trick that US textbook publishers use to prevent their US students from being able to use these cheaper Global/International/Indian edition textbooks in US schools and universities.
In any case, the people hired to change the problem sets have done a botched job, resulting in lots of mistakes.

Since the authors are not collecting those errors, I have listed the ones I discovered below.
If you find others, please feel free to give a pull request.

## For all chapters

The errors in the North American edition are also present in the Global Edition, just that the listed page numbers are offset by 36.
So, for all chapters first refer to [North American edition errata](https://csapp.cs.cmu.edu/3e/errata.html) and add **36** to the page numbers there to get the Global Edition page numbers where you need to fix the errors.

## Chapter 3: Machine-Level Representation of Programs

* Page 233: In the assembly code listing of *Practice Problem 3.10*, the line `movq %rdx, %bax` should be `movq %rdx, %rbx`.

* Page 259: In the assembly code listing of *Practice Problem 3.23*, line 8 should be `subq $2, %rdx`.

* Page 268: In the assembly code listing of *Practice Problem 3.28*, line 3 should be `movl $64, %eax`.

* Page 329: In *Practice Problem 3.49*, the text "let us let s1" should be "let s1".

* Page 335: `[x₁, x₀]` should be `[dx₁, dx₀]`. `[x₀, x₀]` should be `[dx₀, dx₀]`.

* Page 374: In *Solution to Problem 3.30*, the 3rd bullet should read "... case labels 2 and 6 are ...".

* Page 380: In *Solution to Problem 3.42*, the last sentence should read "Function `test` computes the product ...".

* Page 381: In *Solution to Problem 3.44*, the solution to problem A should be `i: 0, c: 4, j: 8, d: 16, Total: 24, Alignment: 8`.
And the solution to problem E should be `a: 0, t: 64, Total: 88, Alignment: 8`.

* Page 381: In *Solution to Problem 3.45*, the solution to problem A the offsets should be `0, 8, 12, 14, 16, 24, 32, 40`.
The solution to problem B is that the total size is 48 bytes.

* Page 384: In *Solution to Problem 3.51*, the instructions for the double->float conversion are `vmovddup %xmm0, %xmm0; vcvtpd2psx %xmm0, %xmm0`.

## Chapter 4: Processor Architecture

* Page 394: In the caption of *Figure 4.3*, the last sentence should read "... as OPq, jXX, rrmovq and cmovXX in Figure 4.2".

* Page 517: In *Solution to Problem 4.1*, in the 3rd bullet the `0x0000010C` should be `0x000000000000010C`.

* Page 518: In *Solution to Problem 4.4*, in the Y86-64 code the `xorq %rax, %rax` should be `irmovq $1, %rax`.
Also, the comment `# If count <= 0, return 1` should be `# If count == 0, return 1`.