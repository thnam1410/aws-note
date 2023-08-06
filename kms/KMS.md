#KMS - Key Management Service

### Key Types:

***Symmetric (AES-256 keys)***
- Single encryption key that is used to Encrypt and Decrypt
- AWS services that are integrated with KMS use Symmetric CMKs
- Never get access to KMS Key unencrypted (must call KMS API to use)


***Asymmetric (RSA & ECC key pairs)***
- Public (Encrypt) and Private Key (Decrypt) pair
- Used for Encrypt/Decrypt - Sign/Verify operations
- The public key is downloadable, but you can't access the Private Key unencrypted

> Use case: Encryption outside of AWS by users who can't call the KMS API


### Types of KMS Keys: ###

- AWS Owned Keys (free): SSE-S3, SSE-SQS, SSE-DDB (default key)
- AWS Managed Key (free): aws/service-name -> Example: aws/rds or aws/ebs
- Customer managed keys created in KMS
- Customer managed keys import (must be symmetric key)


### Automatic Key Rotation: ###
- Automatic every 1 year
- Customer-managed KMS Key (must be enabled): automatic every 1 year
- Imported KMS Key: only manual rotation possible using alias 

### KMS Key Policies: ###
- Control access to KMS Keys
- Similar to S3 bucket policies - Different: Can not control access without them

- Default KMS Key Policy:
  - Created if you don't provide a specific KMS Key Policy
  - Complete access to te key to the root user = entire AWS account
- Custom KMS Key Policy:
  - Define users, roles that can access the KMS Key
  - Define who can administer the key
  - Useful for cross-account access of your KMS Key (different account)







