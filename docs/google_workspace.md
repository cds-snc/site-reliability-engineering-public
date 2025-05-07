# Google Workspace Policies & Configuration

---

## Overview

* Google Workspace settings are managed at two levels:
  * **Organizational Units (OUs)**: Hierarchical structure for core settings
  * **Groups**: Flexible mechanism for granular control
* This presentation outlines best practices for configuration

---

## Core Principles for OU Structure

* **Policy-Driven Structure**: OUs should reflect policy domains, not exact org chart
* **Groups for Granularity**: Use Google Groups for more specific settings
* **Least Privilege**: Grant minimum access needed
* **Automation**: Integrate with HR systems for placement
* **Regular Review**: Periodically assess OU structure alignment

---

## Proposed OU Structure (v1.0)

* **Workspace Administrators**
* **Corporate**
* **Products**
* **Services** (TBC: standard users initially in Corporate)
* **Service Accounts**
* **Transitional**
  * Onboarding
  * Leave of Absence
  * Offboarding

---

## Projected Future OU Structure

* **Workspace Administrators**
* **Corporate** (Finance, HR, Legal, IT, Executive)
* **Products** (Engineering, Product Management, Design, Support)
* **Services** (Consultants, Project Managers, Client Support)
* **Service Accounts** (Application-specific sub-OUs)
* **Transitional** (Onboarding, Leave, Offboarding)

---

## Key OU Policies

* **Workspace Administrators**
  * Mandatory MFA, strong passwords, limited access, detailed auditing
* **Corporate & Products**
  * Standard policies with role-based access via Groups
* **Service Accounts**
  * Strict access controls, limited services, disabled interactive login
* **Transitional**
  * Lifecycle-specific restrictions and configurations

---

## Consultants & Service Accounts

* **Consultants**:
  * Initially manage via Google Group within Services/Corporate OU
  * Create separate OU only if policy needs differ significantly
* **Service Accounts**:
  * Place all in dedicated Service Accounts OU
  * Enforce strict security (limited API access, no interactive login)

---

## Decision Flowchart

1. Is this a service account?
   * Yes → Service Accounts OU
   * No → Continue
2. Is user in transitional state?
   * Yes → Appropriate Transitional sub-OU
   * No → Continue
3. Requires different policies than existing OUs?
   * Yes → Consider new OU
   * No → Use Google Group within existing OU

---

## Core Concepts: OUs vs Groups

* **Organizational Units (OUs)**
  * Primary hierarchical structure
  * Core security and fundamental service settings
  * Settings cascade down hierarchy
* **Groups**
  * Flexible, cross-OU settings
  * Specific service settings or policies
  * Users can belong to multiple groups

---

## Settings Primarily Managed by OUs

* **Security Policies**
  * 2-Step Verification enforcement
  * Password policies
  * Session controls
  * API controls
  * Context-Aware Access
* **Core App Enablement** (enable/disable entire services)
* **Device Management Policies**
* **Chrome Browser Management**
* **Data Regions**

---

## Settings Managed by Either OUs or Groups

* **App Access & Configuration**
  * Google Drive sharing settings
  * Gmail routing and compliance settings
  * Google Chat permissions
  * Meet and Calendar sharing options
  * Vault retention rules
* **Service Settings**
  * Feature-specific controls within core apps

---

## Why Only One Group Can Be Added to OU Settings

* **Preservation of Security Hierarchy**
  * Prevents conflicting policies
  * Maintains clear security model
* **Avoiding Complexity and Overlap**
  * Prevents unresolvable conflicts
  * Ensures policy clarity
* **Targeted Exceptions**
  * Allows for specific exceptions without compromising structure

---

## Key Differences & Use Cases

| Feature   | Organizational Units             | Groups                           |
| --------- | -------------------------------- | -------------------------------- |
| Structure | Hierarchical                     | Non-hierarchical                 |
| Users     | One OU only                      | Multiple groups possible         |
| Purpose   | Core security & service policies | Granular app/feature control     |
| Overrides | Child OUs override parents       | Complement or refine OU settings |

---

## Conclusion

* **OUs**: Provide structural foundation for core security and service availability
* **Groups**: Enable flexible layer for specific apps and features
* Effective strategy combines both approaches:
  * Use OUs for fundamental security posture
  * Use Groups for fine-grained control
* Balance security with flexibility through proper configuration