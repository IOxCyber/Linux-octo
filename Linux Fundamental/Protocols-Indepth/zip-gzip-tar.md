### Compression Commands:
1. **zip**:
   - Purpose: Compress files and directories into a ZIP archive.
   - Syntax: `zip [options] <zipfile> <file1> <file2> ...`
   - Example: `zip archive.zip file1.txt file2.txt`
   - Options: `-r`, `-q`, `-9`, etc.

2. **gzip**:
   - Purpose: Compress files using gzip compression.
   - Syntax: `gzip <file>`
   - Example: `gzip myfile.txt`
   - Decompression: `gzip -d <file>.gz`

3. **tar**:
   - The tar command in Linux is used for creating and manipulating tar archives, which are compressed file archives.
   - The name "tar" stands for "tape archive," as it was originally used to create archives on tape drives. Nowadays, it is commonly used to create and extract archives on disk.
   - Purpose: `to create, view, extract, and manipulate tar archives of files & dirs`
   - Syntax/Example: 
     - Create: `tar -cvf <archive.tar> <file1> <file2> ...`
     - Extract: `tar -xvf <archive.tar>`
    




