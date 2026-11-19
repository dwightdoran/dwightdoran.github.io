# Log Analysis

[All CTF techniques](../ctf-techniques.md)

## My approach

I analyzed web access logs, structured JSON records, Windows event exports, and network flow records with tools including `jq`, `awk`, `grep`, and Python. I started by identifying the fields and record boundaries, then filtered and grouped activity by relevant identifiers.

For web activity, I compared requests, response codes, and transfer information to distinguish probing from evidence of retrieval. For related log sources, I used shared session identifiers to connect events before attributing activity to an account. I examined timing and repetition alongside volume when evaluating unusual behavior.

## What I learned

The question determines the aggregation. Requests, distinct users, active sessions, and transferred bytes are different measurements. I also learned to keep unresolved classifications explicit when the available fields could not support a reliable conclusion.
