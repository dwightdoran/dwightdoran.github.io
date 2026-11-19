# Digital Forensics

[All CTF techniques](../ctf-techniques.md)

## My approach

I used `file`, `xxd`, `strings`, ExifTool, and Binwalk to examine files beyond what their extensions or visible contents suggested. I compared format signatures with internal structure, checked metadata, searched for readable text, and inspected embedded content. When investigating damaged files, I used the expected format structure to guide repairs on a working copy and checked whether the result could be opened correctly.

I also inspected Office documents as containers of XML, metadata, and media. This helped me examine document properties and revision information independently of the application's current display. Git history provided another source of earlier content: a file absent from the working directory could still exist in an earlier commit.

## What I learned

A successful extraction is only a starting point. I need to verify the recovered file's type and contents, distinguish original timestamps from copy or modification times, and preserve the original evidence.
