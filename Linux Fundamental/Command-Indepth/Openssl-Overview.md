## **[Opensshl - Online Book](https://www.feistyduck.com/library/openssl-cookbook/online/):**
- `A cryptography toolkit or command-line tool` that provides implementations of SSL (Secure Sockets Layer) and TLS (Transport Layer Security) protocols.
- `openssl s_client` is the implementation of a simple client that connects to a server using SSL/TLS.
- It implements the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) cryptographic protocols in `HTTPS to secure the web traffic.`

- Example:
```bash
# To initiate an SSL/TLS client connection to a specific server:

openssl s_client -connect 127.0.0.1:30001

The s_client in the openssl command refers to the OpenSSL client, and the -connect option is used to specify the host and port to connect to.
```

## **Basic OpenSSL Commands:**

1. **Generate a Self-Signed Certificate:**
   - Generate a new self-signed certificate with a private key.
   ```bash
   openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365
   ```

2. **Create a Certificate Signing Request (CSR):**
   - Generate a CSR to request a certificate from a CA (Certificate Authority).
   ```bash
   openssl req -new -newkey rsa:4096 -keyout key.pem -out csr.pem
   ```

3. **View Certificate Information:**
   - View details of a certificate.
   ```bash
   openssl x509 -in cert.pem -noout -text
   ```

4. **Check a Certificate's Validity:**
   - Check if a certificate is within its validity period.
   ```bash
   openssl x509 -checkend 86400 -in cert.pem
   ```

5. **Encrypt and Decrypt Files:**
   - Encrypt a file using a symmetric cipher (e.g., AES).
   ```bash
   openssl enc -aes-256-cbc -salt -in plaintext.txt -out encrypted.bin
   ```
   - Decrypt the file.
   ```bash
   openssl enc -d -aes-256-cbc -in encrypted.bin -out decrypted.txt
   ```

6. **Create a Hash (MD5, SHA-256, etc.):**
   - Generate a cryptographic hash of a file.
   ```bash
   openssl dgst -md5 file.txt
   ```

7. **Generate a Random Password:**
   - Generate a random password.
   ```bash
   openssl rand -base64 12
   ```

8. **Convert Certificate Formats:**
   - Convert a certificate from one format to another (e.g., PEM to DER).
   ```bash
   openssl x509 -in cert.pem -outform der -out cert.der
   ```

9. **Create a PKCS#12 (PFX) File:**
   - Create a PKCS#12 file that combines a certificate and its private key.
   ```bash
   openssl pkcs12 -export -out certificate.pfx -inkey key.pem -in cert.pem
   ```

10. **Verify an SSL/TLS Connection:**
    - Connect to a remote server and verify the SSL/TLS connection.
    ```bash
    openssl s_client -connect example.com:443
    ```
