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

## Status
In Progress
