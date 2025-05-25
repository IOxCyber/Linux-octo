# Decompression Commands:

## 1. **unzip**:
   - Purpose: Extract files from a ZIP archive.
   - Syntax: `unzip [options] <zipfile>`
   - Example: `unzip archive.zip`

## Options: `-d`, `-l`, `-q`, `-o`:

1. **Basic Usage**:
   To extract a ZIP archive, use the following syntax:
   ```bash
   unzip <archive.zip>
   ```
  > This will extract the contents of the ZIP archive into the current directory.

2. **Extract to a Specific Directory**:
   If you want to extract the contents of the ZIP archive to a specific directory, use the `-d` option followed by the destination directory:
   ```bash
   unzip <archive.zip> -d <destination_directory>
   ```

3. **List Contents of ZIP Archive**:
   To list the contents of a ZIP archive without extracting it, use the `-l` option:
   ```bash
   unzip -l <archive.zip>
   ```

4. **Extract Specific Files**:
   You can specify which files or directories to extract from the ZIP archive by providing their names as arguments:
   ```bash
   unzip <archive.zip> <file1> <file2> ...
   ```

5. **Extract with Overwrite**:
   By default, `unzip` will prompt before overwriting files. To overwrite existing files without prompting, use the `-o` option:
   ```bash
   unzip -o <archive.zip>
   ```

6. **Quiet Mode**:
   Suppress output during extraction with the `-q` option:
   ```bash
   unzip -q <archive.zip>
   ```

## 5. **gunzip**:
   - Purpose: Decompress files compressed with gzip.
   - Syntax: `gunzip <file>.gz`
   - Example: `gunzip myfile.txt.gz`

### Options:
1. If you want to keep the original file and create a new uncompressed file, you can use the `-k` or `--keep` option:

```bash
gunzip -k file.gz
```

Or:

```bash
gunzip --keep file.gz
```
2. You can also use `gzip` with the `-d` or `--decompress` option, which performs the same function as `gunzip`:

```bash
gzip -d file.gz
```

Or:

```bash
gzip --decompress file.gz
```


6. **tar**:
   - Purpose: Extract files from tar archives.
   - Syntax: `tar -xvf <archive.tar>`
   - Example: `tar -xvf archive.tar`
