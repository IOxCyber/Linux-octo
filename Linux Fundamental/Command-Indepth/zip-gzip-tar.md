### Compression Commands: 

## 1. **tar**: `Bundles files and directories into a single NON-COMPRESSED archive file`
   - The name "tar" stands for "tape archive," as it was originally used to create archives on tape drives.
   - Purpose: `to create, view, extract, and manipulate tar archives of files & dirs`
   - Syntax/Example: 
     - Create: `tar -cvf <archive.tar> <file1> <file2> ...`
     - Extract: `tar -xvf <archive.tar>`

### Other Options: `Compressed Tar`
- Create a Compressed Archive (gzip):
`tar -czvf archive.tar.gz file1 file2 directory1`

- Create a Compressed Archive (bzip2):
`tar -cjvf archive.tar.bz2 file1 file2 directory1`

- List Contents of an Archive:
`tar -tvf archive.tar`

- Append Files to an Existing Archive:
`tar -rvf archive.tar newfile`

- Extract Specific Directory from an Archive:
`tar -xvf archive.tar -C /path/to/directory directory1`


## 2. **zip**: `Compress multiple files and directories into a single compressed archive`
   - Purpose: Compress files and directories into a ZIP archive.
   - Syntax: `zip [options] <zipfile> <file1> <file2> ...`
   - Example: `zip archive.zip file1.txt file2.txt`

### Options: `-r`, `-q`, `-9`, etc.
- Password Protection, -P option followed by a password to encrypt the archive: compressed & Encrypted file: `zip -P password archive.zip file1.txt file2.txt`
- Recursive Compression: To include all files and subdirectories within a directory, use the -r option: `zip -r archive.zip directory/`
- 0: No compression. Files are stored without any compression. This option is useful if you only want to archive files without compressing them.
- 1 to -8: These levels represent varying degrees of compression, with -1 being the fastest (least compression) and -8 offering higher compression at the expense of speed.
- 9: Maximum compression. This level provides the highest compression ratio but may take longer to compress files compared to lower levels.


## 3. **gzip**: `Compressing individual files`
   - Purpose: Compress files using gzip compression.
   - Syntax: `gzip <file>`
   - Example: `gzip myfile.txt`
   - Decompression: `gzip -d <file>.gz`

### Options:
- `-c`, `--stdout`: Write output to standard output and keep original files unchanged.
- `-d`, `--decompress`: Decompress the compressed file(s).
- `-f`, `--force`: Force compression or decompression, even if it would overwrite existing files.
- `-r`, `--recursive`: Recursively compress or decompress directories.
- `-t`, `--test`: Test the integrity of the compressed file(s).
- `-v`, `--verbose`: Display verbose output.
- `-1`, `-9`: Compression level (1 for fastest, 9 for best compression, default is 6).

### Examples:
1. Compress a file:
   ```bash
   gzip file.txt
   ```
   This command compresses `file.txt` and creates a new file named `file.txt.gz`.

2. Decompress a file:
   ```bash
   gzip -d file.txt.gz
   ```
   This command decompresses `file.txt.gz` and restores the original `file.txt`.

3. Compress multiple files:
   ```bash
   gzip file1.txt file2.txt
   ```
   This command compresses `file1.txt` and `file2.txt` individually.

4. Compress a file and keep the original:
   ```bash
   gzip -c file.txt > file.txt.gz
   ```
   This command compresses `file.txt` and writes the compressed output to `file.txt.gz` while keeping the original `file.txt` unchanged.

5. Recursively compress all files in a directory:
   ```bash
   gzip -r directory
   ```
   This command compresses all files in the `directory` recursively.

6. Test the integrity of a compressed file:
   ```bash
   gzip -t file.txt.gz
   ```
   This command tests the integrity of `file.txt.gz` without decompressing it.



---
> ## tar vs zip vs gzip:
---
| Feature              | tar                                      | zip                                      | gzip                                     |
|----------------------|------------------------------------------|------------------------------------------|------------------------------------------|
| Purpose              | Archive files and directories            | Archive files and directories            | Compress files                            |
| Compression          | Optional (requires additional options)   | Yes                                      | Yes                                      |
| File Format          | Uncompressed (tar) or optionally compressed (tar.gz, tar.bz2) | Compressed (zip)                          | Compressed (gzip)                         |
| Support for Multiple Files/Directories | Yes                                  | Yes                                      | No (compresses individual files)         |
| Directory Structure Preservation | Yes                                 | Yes                                      | No                                       |
| Platform Compatibility | Cross-platform (common on Unix-like systems) | Cross-platform                           | Cross-platform                           |
| File Extension       | .tar, .tar.gz, .tar.bz2                   | .zip                                     | .gz                                      |
| Usage                | Create and extract archives               | Create and extract archives               | Compress and decompress individual files |
| Command Examples     | - Create: `tar -cvf archive.tar file1 file2 directory1` | - Create: `zip archive.zip file1 file2 directory1` | - Compress: `gzip file.txt`<br>- Decompress: `gzip -d file.txt.gz` |



