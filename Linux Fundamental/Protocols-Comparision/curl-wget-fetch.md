1. curl: Best for flexible data transfer tasks, scripting, API interaction, and when dealing with multiple protocols.
2. wget: Best for downloading large numbers of files, recursive downloads, or when network stability is a concern.
3. fetch: A simpler tool for basic file retrieval, commonly found in FreeBSD systems, but less feature-rich than curl or get.


# Command Line Tools for File Transfer in Linux

## 1. `curl` (Client URL)

`curl` is a command-line tool used to transfer data from or to a server using various protocols.

### Basic Commands

- **Download a file:**
  ```bash
  curl -O http://example.com/file.txt
  ```

- **Download and save to a specific filename:**
  ```bash
  curl -o output.txt http://example.com/file.txt
  ```

- **Send data with POST request:**
  ```bash
  curl -X POST -d "key=value" http://example.com/submit
  ```

- **Use basic authentication:**
  ```bash
  curl -u username:password http://example.com/protected
  ```

## 2. `wget` (Web Get)

`wget` is a command-line utility for downloading files from the web.

### Basic Commands

- **Download a file:**
  ```bash
  wget http://example.com/file.txt
  ```

- **Recursive download of a website:**
  ```bash
  wget -r http://example.com/
  ```

- **Resume a partially downloaded file:**
  ```bash
  wget -c http://example.com/file.txt
  ```

- **Download using a specific User-Agent:**
  ```bash
  wget --user-agent="Mozilla/5.0" http://example.com/
  ```

## 3. `fetch`

`fetch` is a command primarily used in FreeBSD for simple file retrieval.

### Basic Commands

- **Download a file:**
  ```bash
  fetch http://example.com/file.txt
  ```

- **Download and save to a specific filename:**
  ```bash
  fetch -o output.txt http://example.com/file.txt
  ```


