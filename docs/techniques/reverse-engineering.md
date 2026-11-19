# Reverse Engineering

[All CTF techniques](../ctf-techniques.md)

## My approach

I inspected source code, Python and Java bytecode, and native executables to understand input validation. Ghidra helped me follow references from readable strings into relevant functions; bytecode inspection and decompilation helped expose comparisons and control flow in other formats.

I broke validation into smaller constraints: input length, character positions, numerical representations, arithmetic, and bitwise operations. I traced early returns and failure branches before assuming a rule applied to every input. Where possible, I checked a candidate against the original validation logic rather than accepting readable output alone.

## What I learned

Decompiled code is an aid to analysis, not a guaranteed reconstruction of the original source. Runtime versions, integer behavior, and evaluation order matter. A partial reconstruction remains partial until the relevant checks have been verified.
