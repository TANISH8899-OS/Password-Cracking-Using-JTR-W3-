# John the Ripper (JTR) — Notes and Commands

These notes are for an authorized local lab only. The screenshots supplied for this project show the **Johnny GUI on Windows**; they do not document a complete command-line run. The examples below are general JTR usage references, not claims that these exact commands were run in the screenshots.

## Verify the installation

On a system where John the Ripper is installed and available in the terminal:

```bash
john --version
john --list=formats
```

If `john` is not on your PATH, run it using the full path to the executable.

## Check a hash file

Keep the hash file in your lab directory and ensure it contains only test data you are authorized to audit. Avoid committing sensitive hashes to GitHub.

## Run a controlled dictionary audit

General syntax:

```bash
john --wordlist=<path-to-authorized-wordlist> <path-to-test-hash-file>
```

Replace both placeholders with paths to your own lab files. Do not use this against accounts, systems, or files without permission.

## Review the result

```bash
john --show <path-to-test-hash-file>
```

## Important notes

- The exact supported format depends on the John the Ripper build.
- PDF hash extraction tools may produce formats that require a compatible JTR Jumbo build.
- Never place real credentials, private hashes, or confidential documents in this repository.
- The supplied POC screenshots show the Johnny graphical workflow; they do not establish that the CLI commands above were executed.
