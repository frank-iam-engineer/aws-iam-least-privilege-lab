# Security Findings

## 1. Overly Broad AssumeRole Permissions
Using `"Resource": "*"` in a user AssumeRole policy can allow unintended access to sensitive roles.

## 2. Broad Trust Policies
Trusting `arn:aws:iam::<account-id>:root` is broader than trusting a specific user or role and increases the attack surface.

## 3. Role Chaining Risk
If a low-privilege role can assume a higher-privilege role, that creates a privilege escalation path.

## 4. Least Privilege Design
Each role should only contain the exact actions required for the job function.
