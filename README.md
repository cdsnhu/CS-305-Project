### Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?
Artemis Financial is a consulting company that develops individualized financial plans for its customers. Financial plans include savings, retirement, investments, and insurance. The company is seeking to know how to protect its client data and financial information.

### What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?
Through reading the resource materials and understanding basic security implementations, like encryption, hashing, and checksums, I was able to understand how data can be safely secured and to apply them to software. Creating secure code is essential to any data exposed to the internet, as there exist so many exploits and methods for attackers to manipulate computers, such as databases and websites. When using sensitive data, such as banking and personal information, designing security protocols is not only strongly enforced, it is legally required, as these kinds of data are extremely valuable to attackers and can cause irreversible damage to clients if compromised.

### Which part of the vulnerability assessment was challenging or helpful to you?
Creating the CA and applying it to the Spring Boot was challenging; I was not made aware of the properities file required for it.
A helpful tool to use was the OWASP report, a versatile tool to assist with discovering reported CVEs that the packages might contain. Along with how to suppress CVEs, with proper justification, that might not be relevant to the overall project.

### How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?
Encryption was one technique to use, using RSA-384 for TLS with the generated CA. Along with generating a checksum using the SHA-256 hashing function to verify data integrity without exposing or compromising the data held within. Although encryption for data at rest was not used, AES encryption would be an ideal method to safeguard data at rest. If we were using a SQL database, using proper parameterized queries is a requirement to prevent SQL injections.

### How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
By running tests to see if the site not only operated but also proper security methods were working as well. Displaying the hash method on the website to verify checksum verification.

### What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
In this project, the Spring Boot documentation was a valuable resource when faced with syntax issues or how to utilize the package's functionalities. The OWASP website is an encyclopedia of reported CVE vulnerabilities that can help prevent future issues from occurring

### Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?
How to implement basic security measures: 
  Encryption, both symetrical and asymetrical
    Creating CAs and understanding their relevance to the client's trust in a domain/business
  Checksums: SHA-256 hash to verify data integrity
