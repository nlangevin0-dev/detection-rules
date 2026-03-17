# Detection Rules

Sigma detection rules for AWS CloudTrail security monitoring, mapped to MITRE ATT&CK.

## Rules

| Rule | Description | Severity | ATT&CK |
|------|-------------|----------|--------|
| unauthorized_api_call.yml | Detects AccessDenied errors indicating potential credential misuse | Medium | T1087 - Account Discovery |
| iam_user_created.yml | Detects new IAM user creation indicating possible persistence | High | T1136.003 - Create Account: Cloud |
| root_account_usage.yml | Detects root account API usage outside console login | Critical | T1078.004 - Valid Accounts: Cloud |

## Usage

Convert to Splunk:
```
sigma convert -t splunk --without-pipeline unauthorized_api_call.yml
```

## Requirements

- sigma-cli
- pySigma-backend-splunk
```
