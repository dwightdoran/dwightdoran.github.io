# Password Auditing

[All CTF techniques](../ctf-techniques.md)

## My approach

I used Hashcat and John the Ripper to test password candidates against authorized local hashes and protected files. Before selecting an attack, I identified the format from its structure and context. I used format-specific extraction tools when a protected file needed to be converted into input the auditing tool could process.

I practiced dictionary, rule, mask, and hybrid approaches. Where evidence supported a password pattern, I narrowed the candidate space and checked the generated candidates before running the test. I also used Python to express candidate transformations precisely instead of relying on manual guesses.

## What I learned

An exhausted candidate set is not proof that recovery is impossible. I checked progress, rejected candidates, and recovery output to distinguish a completed test from a run that had not processed useful input. Recovery claims required a matching hash or successful decryption.
