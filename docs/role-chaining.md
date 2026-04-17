# Role Chaining

## Overview
This project demonstrates role chaining in AWS IAM.

Flow:
frank-iam-engineer → Dev-ReadOnly-Role → EC2-Admin-Role

## Explanation
- The user assumes a low-privilege role (Dev)
- The Dev role is allowed to assume a higher-privilege role (EC2 Admin)
- This simulates how privilege escalation paths can exist in real environments

## Security Risk
If not controlled properly, role chaining can allow users to escalate privileges beyond their intended access level.

## Mitigation
- Restrict which roles can assume other roles
- Apply least privilege
- Monitor STS usage
