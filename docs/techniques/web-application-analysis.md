# Web Application Analysis

[All CTF techniques](../ctf-techniques.md)

## My approach

I used browser developer tools and `curl` to understand normal application behavior before testing a hypothesis. I inspected requests, response headers, page source, loaded resources, cookies, and client-side state. Comparing a baseline request with a controlled change helped me identify which inputs affected server behavior.

My notes include practice with access-control weaknesses, file-path handling, injection, and unsafe handling of serialized data. I focused on the underlying trust boundaries: whether the server trusted a client-supplied value, whether authorization was enforced at the relevant resource, and whether errors disclosed implementation details.

## What I learned

Encoding does not provide integrity protection, and browser-side checks cannot establish server-side authorization. I also distinguished rendered HTML from demonstrated script execution and kept inferred backend behavior separate from behavior I could directly observe.
