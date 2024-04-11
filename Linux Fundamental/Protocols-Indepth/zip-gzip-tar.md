### Compression Commands: 

1. **tar**: `Bundles files and directories into a single NON-COMPRESSED archive file`
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



2. **zip**: `Compress multiple files and directories into a single compressed archive`
   - Purpose: Compress files and directories into a ZIP archive.
   - Syntax: `zip [options] <zipfile> <file1> <file2> ...`
   - Example: `zip archive.zip file1.txt file2.txt`
   - Options: `-r`, `-q`, `-9`, etc.


3. **gzip**: `Compressing individual files`
   - Purpose: Compress files using gzip compression.
   - Syntax: `gzip <file>`
   - Example: `gzip myfile.txt`
   - Decompression: `gzip -d <file>.gz`

    
## tar vs zip vs gzip:

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



