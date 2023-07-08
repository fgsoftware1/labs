=====================
Local File Inclusion Lab
=====================

Tasks
=====

1. Task 1: Exploiting Local File Inclusion
-------------------------------------------

- Exploit the Local File Inclusion vulnerability to retrieve sensitive files from the server.
- Use different techniques and payloads to include files, such as `/etc/passwd` or `/etc/shadow`.
- Document the steps you took to successfully exploit the vulnerability.

2. Task 2: Patching the Vulnerability
-------------------------------------

- Implement the necessary fixes to prevent further Local File Inclusion attacks.
- Describe the security measures you applied to mitigate the vulnerability.
- Explain how these measures prevent unauthorized access to sensitive files.

Writeup
=======

Introduction
-------------

In this lab, we explored the Local File Inclusion (LFI) vulnerability and its potential impact on a web application. The LFI vulnerability allows an attacker to include and execute files from the server, potentially exposing sensitive information or leading to remote code execution.

Task 1: Exploiting Local File Inclusion
--------------------------------------

To begin, we identified the LFI vulnerability in the target web application. By manipulating the input parameter, we were able to trick the server into including arbitrary files. We experimented with different payloads and techniques to retrieve sensitive files, such as `/etc/passwd` and `/etc/shadow`.

The exploitation process involved carefully crafting the input to bypass input sanitization and directory traversal restrictions. We used techniques like null bytes, URL encoding, and relative path traversal to successfully retrieve the desired files. Throughout the process, we documented the payloads used and the results obtained.

Task 2: Patching the Vulnerability
----------------------------------

After successfully exploiting the LFI vulnerability, we proceeded to implement necessary fixes to patch the vulnerability. We applied several security measures to prevent further Local File Inclusion attacks:

1. Input Validation and Sanitization: We implemented strict input validation and sanitization routines to ensure that user-supplied input does not contain malicious characters or file paths.
2. Whitelist Approach: Instead of trying to blacklist disallowed characters or file paths, we used a whitelist approach to explicitly specify the allowed input values.
3. Access Control: We reviewed the file inclusion logic and restricted access to sensitive files by implementing appropriate access control mechanisms.

By implementing these measures, we effectively mitigated the Local File Inclusion vulnerability and reduced the risk of unauthorized file access and remote code execution.

Conclusion
----------

The Local File Inclusion lab provided valuable insights into the risks associated with this type of vulnerability and the techniques used to exploit and mitigate it. By understanding the attack vectors and implementing robust security measures, we can safeguard web applications against Local File Inclusion attacks and maintain the confidentiality and integrity of sensitive data.

