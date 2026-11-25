# CIA Triad

CIA is one of the most important fundamental principles in cybersecurity and cloud security engineering. It is a model that identifies three main objectives that any system, application, or infrastructure must protect to ensure information security.

The acronym CIA stands for three concepts:

1. **Confidentiality**
2. **Integrity**
3. **Availability**

---

## 1. Confidentiality

This means ensuring that information can only be accessed or viewed by authorized individuals or systems; in other words, protecting data from unauthorized access.

This data includes:

- Passwords
- Personal data
- Financial information
- Cloud service access credentials
- Customer files

### Methods to Achieve Confidentiality

- **Encryption:** Helps encrypt data to prevent it from being read without the appropriate key.
- **IAM:** Determines who has access to resources.
- **MFA:** Adds an extra layer of security when logging in.
- **Access Control:** Defines user permissions.
- **Least Privilege:** Gives users only the minimum permissions they need.

### Example

A file containing customer data is stored on Amazon S3. If you restrict file permissions to specific individuals only and use encryption, you are applying confidentiality.

Another example: If you make the S3 bucket public and anyone can read customer data, this is a breach of confidentiality.

---

## 2. Integrity

This means ensuring that data remains accurate and complete and has not been tampered with or altered without permission; in simpler terms, making sure that data has not been changed without authorization.

### Why Do We Need It?

To ensure data reliability and accuracy, especially regarding:

1. Financial transactions
2. Customer databases
3. System logs
4. Backup files
5. Cloud infrastructure settings

### Methods to Achieve Integrity

- **Hashing:** Creates a digital footprint of the data to detect changes.
- **Digital Signatures:** Verify the source and integrity of the data.
- **Checksums:** Detect errors and changes in data.

### Example

If you have a file saved on Amazon S3, you can create a digital fingerprint for the file using SHA-256.

If the file is modified, the digital fingerprint will change, thus confirming that the file is not identical to the original version.

---

## 3. Availability

This means ensuring that systems, applications, and data are available to authorized users when they need them. In simpler terms, making sure that services are available and accessible at the required time.

### Why Do We Need It?

To prevent service interruptions and business disruptions such as:

1. Websites
2. Banking applications
3. Cloud services
4. Databases
5. Systems that require continuous operation

### Methods to Achieve Availability

- **Backups:** Create backups to restore data.
- **High Availability:** Designs systems to continue functioning even if one of their components fails.
- **Load Balancing:** Distributes requests across multiple servers.
- **Auto Scaling:** Increases or decreases resources as needed.
- **Disaster Recovery:** Restores systems after disasters.
- **DDoS Protection:** Protects against denial-of-service attacks.
- **Multi-AZ:** Distributes resources across different Availability Zones.

### Example

You have a website running on EC2 in a single Availability Zone. If this zone fails, the website will stop working.

However, if you use more than one Availability Zone with load balancing, the website will continue to work even if one of these Availability Zones fails.
