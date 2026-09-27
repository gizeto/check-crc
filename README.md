# check-crc

Tiny helper to verify a file's CRC32 against srrdb.com and optionally rename it back to the original release filename.

## Install

Requires Python 3.x (only standard library modules are used).

```bash
wget -O /usr/local/bin/check-crc https://raw.githubusercontent.com/gizeto/check-crc/main/check-crc
chmod +x /usr/local/bin/check-crc
```

If you already cloned this repo, you can link the script instead:

```bash
chmod +x check-crc
ln -sfn "$(pwd)/check-crc" /usr/local/bin/check-crc
```

## Usage

```bash
check-crc <file-or-directory> [--rename]
```

- Use a directory to check all non-sample files inside (skipping .nfo/.sfv/.srr/.nzb).
- Add `--rename` to rename a matching file to the original release filename.
- Trailing copy suffixes such as ` (1)` or ` (2)` before the extension are ignored when looking up files on srrDB.
