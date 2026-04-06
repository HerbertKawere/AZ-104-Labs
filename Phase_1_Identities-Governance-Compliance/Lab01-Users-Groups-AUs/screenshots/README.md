# Lab 1 – Azure AD Users, Groups, and Administrative Units

---

## Objective

Build an enterprise-grade identity foundation in Microsoft Azure using the Azure Portal, covering:

- Azure AD user creation  
- Security groups (assigned and dynamic)  
- Administrative Units (AUs)  
- Scoped role assignment using AUs  

---

## What Was Done

### 🔹 Users
- Created 4 users: `bena`, `bena HR`, `herbert`
- Set the **Department** attribute for each user to support dynamic group filtering

### 🔹 Groups
- Created an assigned security group: **HR Staff**
- Created a dynamic security group: **bena HR** using the department attribute
- Added members manually to the assigned group
- Verified automatic membership in the dynamic group

### 🔹 Administrative Unit (AU)
- Created **HR Department AU**
- Scoped `bena HR` under the AU

### 🔹 Scoped Role Assignment
- Assigned the **User Administrator** role to `bena HR`
- Scoped the role exclusively to the HR Department AU
- Ensured admin permissions apply only to HR-related users

---

## 📸 Screenshots

Located in `/screenshots/`

**Recommended screenshots to include:**

✅ Users list – `01-create-users.png`  
✅ Group creation and membership – `02-create-group-assigned.png`  
✅ Dynamic group rule – `03-dynamic-group-rule.png`  
✅ Administrative Unit structure – `04-au-creation.png`  
✅ Scoped role assignment screen – `05-au-role-assignment.png`  

---

## 🔐 Security Insight

Scoped administration using Administrative Units enforces **least privilege access**:

- `bena HR` **cannot view or modify users outside** the HR Department AU  
- This mirrors **real enterprise role delegation** in large organizations  

This lab demonstrates how to:
- Reduce lateral movement
- Limit administrative blast radius
- Control exposure in multi-admin Azure environments  

A foundational skill for any **cloud or identity security engineer**.

---

## 🧹 Clean-up Instructions

To avoid unnecessary resource usage:

- Delete test users (`bena`, `bena HR`, `herbert`)
- Delete security groups (**HR Staff**)
- Remove role assignments from the AU
- Delete the Administrative Unit after users and roles are removed

---

## 🔗 Linked Labs


This lab builds the foundation to move into **fine-grained access control** using custom roles and RBAC.
