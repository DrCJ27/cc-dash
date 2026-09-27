# cc-dash

Static shell for the Command Center dashboards.

Every `*.json` file here is an **AES-256-GCM ciphertext blob** — salt, IV and
ciphertext, nothing else. No readable content is stored in this repo. The page
derives a key with PBKDF2-SHA256 (250k iterations) from a passphrase entered in
the browser and decrypts locally; the passphrase is never transmitted.

The repo is public only because GitHub Pages for private repos requires a paid
plan. Publishing plaintext here would expose athlete health details and phone
numbers, so it is never done.

Written by `scripts/sweeplib/publish_web.py` in the command-center repo.
