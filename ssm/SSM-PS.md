#SSM Parameter Store

Features:

- Force rotation of secrets every X days
- Automate generation of secret on rotation (Lambda)
- Integration with RDS (MySQL, PostgreSQL, Aurora)
- Secrets are encrypted by KMS

### Multi-Region Secrets

- Replicate Secrets across multiple AWS accounts
- Secrets Manager keeps read replicas in sync with the primary secret
- Ability to promote a read replica secret to a standalone secret

Use cases: multi-region apps, disaster recovery, multi-region DB
