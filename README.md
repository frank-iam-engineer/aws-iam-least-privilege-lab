# AWS IAM Least Privilege Lab

## Overview
This project demonstrates real-world AWS IAM design using users, roles, trust policies, and permission policies.

It focuses on:
- Least privilege access
- Role-based access control
- Secure trust relationships
- Role assumption using STS
- Identification of IAM misconfigurations

---

## Architecture

byte-user
  ├── Dev-ReadOnly-Role
  ├── QA-Role
  └── Admin-Role

Dev-ReadOnly-Role
  └── EC2-Admin-Role (role chaining)

---

## Goals
- Replace direct user permissions with role assumption
- Enforce least privilege
- Demonstrate role chaining
- Identify and fix security flaws

---

## Evidence

This repository includes CLI evidence showing:
- Base IAM user identity
- Successful role assumption into Dev-ReadOnly-Role
- Successful role chaining into EC2-Admin-Role
- Permission-based success and failure cases

## Key IAM Concepts Demonstrated
- Least privilege
- Trust policy vs permission policy
- STS temporary credentials
- Role assumption
- Role chaining
- IAM misconfiguration analysis

- ## Status
In progress


## Security Lessons
- Broad `sts:AssumeRole` permissions create escalation risk
- Broad trust policies expand attack surface
- Role chaining must be tightly controlled
- Permissions and trust must both be reviewed during IAM audits
