# AWS IAM Least Privilege Lab

## Overview
This project demonstrates practical AWS IAM engineering, focusing on least privilege access, role-based access control, and secure identity design using AWS STS.

It simulates how real organizations manage access using roles instead of direct user permissions.

---

## Architecture

Frank_IAM
  ├── Dev-ReadOnly-Role
  ├── QA-Role
  └── Admin-Role

Dev-ReadOnly-Role
  └── EC2-Admin-Role (role chaining)

---

## Key Features
- Role-based access control (RBAC)
- Least privilege enforcement
- Trust policy vs permission policy separation
- Role assumption using AWS STS
- Role chaining simulation
- CLI-based validation and testing

---

## Evidence
This project includes CLI-based proof of:

- Base IAM identity
- Successful role assumption
- Role chaining across multiple roles
- Permission-based success and failure scenarios

---

## Security Insights

### 1. Trust vs Permission
A role must both trust an identity AND the identity must have permission to assume it.

### 2. Role Chaining Risk
Low-privilege roles can escalate privileges if allowed to assume higher-privilege roles.

### 3. Over-Permission Risk
Using wildcard (`*`) in IAM policies increases attack surface.

### 4. Access Control Precision
Permissions like `s3:GetObject` and `s3:ListAllMyBuckets` must be explicitly defined.

---

## Lessons Learned
- IAM is about controlling "who can access what"
- Trust and permission must both be configured correctly
- Error messages help identify permission vs configuration issues
- Real validation requires CLI testing, not just policy writing

---

## Author
Frank_IAM — IAM Engineer focused on identity security, least privilege, and real-world access control design
