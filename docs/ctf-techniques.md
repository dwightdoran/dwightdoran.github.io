# CTF Techniques

My CTF practice has strengthened how I investigate unfamiliar systems: identify the evidence, form a testable explanation, choose a focused tool, and verify the result. These are transferable techniques from my competition and practice notes, described at the skill level without reproducing challenge prompts, artifacts, answers, or solution paths.

## File triage and digital forensics

I used `file`, `xxd`, `strings`, ExifTool, and Binwalk to examine files beyond what their extensions or visible contents suggested. I compared format signatures with internal structure, checked metadata, searched for readable text, and inspected embedded content. When investigating damaged files, I used the expected format structure to guide repairs on a working copy and checked whether the result could be opened correctly.

I also inspected Office documents as containers of XML, metadata, and media. This helped me examine document properties and revision information independently of the application's current display. Git history provided another source of earlier content: a file absent from the working directory could still exist in an earlier commit.

**What I learned:** a successful extraction is only a starting point. I need to verify the recovered file's type and contents, distinguish original timestamps from copy or modification times, and preserve the original evidence.

## Log analysis and event correlation

I analyzed web access logs, structured JSON records, Windows event exports, and network flow records with tools including `jq`, `awk`, `grep`, and Python. I started by identifying the fields and record boundaries, then filtered and grouped activity by relevant identifiers.

For web activity, I compared requests, response codes, and transfer information to distinguish probing from evidence of retrieval. For related log sources, I used shared session identifiers to connect events before attributing activity to an account. I examined timing and repetition alongside volume when evaluating unusual behavior.

**What I learned:** the question determines the aggregation. Requests, distinct users, active sessions, and transferred bytes are different measurements. I also learned to keep unresolved classifications explicit when the available fields could not support a reliable conclusion.

## Network traffic analysis

I used Wireshark to narrow packet captures by protocol, endpoint, and conversation. Rather than treating each packet in isolation, I followed exchanges and considered request direction, response direction, and the layer where a field belonged.

My practice included interpreting name resolution, time synchronization, host identity, and wireless management traffic. I documented methods for reconstructing application streams and working with authorized decryption material when available. These exercises reinforced the difference between what a packet directly shows and what a vendor lookup or service convention merely suggests.

**What I learned:** accurate attribution needs context. A network interface vendor does not necessarily identify the complete device, and a familiar port does not establish the actual application. Capture location, packet order, and protocol fields all affect the interpretation.

## Offline password auditing

I used Hashcat and John the Ripper to test password candidates against authorized local hashes and protected files. Before selecting an attack, I identified the format from its structure and context. I used format-specific extraction tools when a protected file needed to be converted into input the auditing tool could process.

I practiced dictionary, rule, mask, and hybrid approaches. Where evidence supported a password pattern, I narrowed the candidate space and checked the generated candidates before running the test. I also used Python to express candidate transformations precisely instead of relying on manual guesses.

**What I learned:** an exhausted candidate set is not proof that recovery is impossible. I checked progress, rejected candidates, and recovery output to distinguish a completed test from a run that had not processed useful input. Recovery claims required a matching hash or successful decryption.

## Web application analysis

I used browser developer tools and `curl` to understand normal application behavior before testing a hypothesis. I inspected requests, response headers, page source, loaded resources, cookies, and client-side state. Comparing a baseline request with a controlled change helped me identify which inputs affected server behavior.

My notes include practice with access-control weaknesses, file-path handling, injection, and unsafe handling of serialized data. I focused on the underlying trust boundaries: whether the server trusted a client-supplied value, whether authorization was enforced at the relevant resource, and whether errors disclosed implementation details.

**What I learned:** encoding does not provide integrity protection, and browser-side checks cannot establish server-side authorization. I also distinguished rendered HTML from demonstrated script execution and kept inferred backend behavior separate from behavior I could directly observe.

## Reverse engineering and program reasoning

I inspected source code, Python and Java bytecode, and native executables to understand input validation. Ghidra helped me follow references from readable strings into relevant functions; bytecode inspection and decompilation helped expose comparisons and control flow in other formats.

I broke validation into smaller constraints: input length, character positions, numerical representations, arithmetic, and bitwise operations. I traced early returns and failure branches before assuming a rule applied to every input. Where possible, I checked a candidate against the original validation logic rather than accepting readable output alone.

**What I learned:** decompiled code is an aid to analysis, not a guaranteed reconstruction of the original source. Runtime versions, integer behavior, and evaluation order matter. A partial reconstruction remains partial until the relevant checks have been verified.

## Encoding and cryptography fundamentals

I used CyberChef and Python to work with text encodings, classical ciphers, XOR transformations, and small educational RSA examples. My first step was to identify the representation of the input so that an encoding layer was not mistaken for encryption.

I practiced reversing transformations and checking results against the original operation. This work strengthened my understanding of how keys, byte representations, and operation order affect an analysis, as well as why an apparently readable fragment is weak evidence on its own.

**What I learned:** choose a method based on the data and verify the full result. Small educational examples illustrate cryptographic concepts; they do not demonstrate an ability to break properly implemented modern encryption.

## Open-source research and corroboration

I combined focused searches with vendor documentation, public records, metadata inspection, DNS queries, and certificate inspection. I used tools such as ExifTool, `dig`, and OpenSSL to inspect technical evidence, then checked relevant findings against independent sources.

I paid particular attention to exact model identifiers, hardware revisions, dates, and source provenance. A current product description or search result may not describe the version or time period under investigation.

**What I learned:** research is strongest when the conclusion has a traceable basis. I distinguish an exact match from a plausible lead and document conflicting evidence instead of hiding it.

## Investigation habits I carry forward

I keep notes organized around the question, observation, action, result, and next step. Recording unsuccessful tests helps prevent repeated work and makes it easier to explain why I changed direction. Small scripts help with repetitive parsing and verification, while manual inspection keeps the automation tied to the evidence.

I distinguish a locally reproduced result from a competition-confirmed answer. Unresolved work stays unresolved in my notes. The most useful outcome of this practice is a more disciplined way to investigate, explain uncertainty, and communicate findings.
