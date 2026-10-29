 🛡️ Linux Hardening & Web Security Checklists

A comprehensive, production-ready security checklist and hardening guide for Linux server environments and web application security assessments (OWASP Top 10).

---

## 🐧 Part 1: Linux Server Hardening Checklist
Essential steps to secure a fresh Linux installation and reduce the attack surface:

- [ ] **1. User & Access Management**
  - [ ] Disable root login via SSH (`PermitRootLogin no`).
  - [ ] Enforce SSH Key-Based Authentication and disable password authentication.
  - [ ] Audit and remove unused default user accounts.
  - [ ] Enforce strong password policies and expiration rules (`pam_pwquality`).

- [ ] **2. Network & Firewall Configuration**
  - [ ] Configure and enable a firewall (`UFW` or `iptables`).
  - [ ] Close all unnecessary listening ports (`ss -tulpn`).
  - [ ] Disable IPv6 if not actively required in the environment.

- [ ] **3. System Updates & Patching**
  - [ ] Enable automatic security updates or establish a regular patching schedule.
  - [ ] Remove obsolete or unmaintained packages and services (e.g., Telnet, FTP).

- [ ] **4. Logging & Monitoring**
  - [ ] Ensure system auditing (`auditd`) is active and tracking critical files.
  - [ ] Configure remote syslog forwarding or centralized log monitoring.

---

## 🌐 Part 2: OWASP Top 10 Web Security Checklist
Key risk categories and validation checks for web applications:

- [ ] **A01: Broken Access Control**
  - [ ] Verify vertical and horizontal privilege escalation controls.
  - [ ] Ensure direct object references (IDOR) are properly protected with authorization checks.

- [ ] **A02: Cryptographic Failures**
  - [ ] Enforce HTTPS (TLS 1.2 / 1.3) across the entire application.
  - [ ] Ensure sensitive data (passwords, tokens, PII) is hashed or encrypted at rest.

- [ ] **A03: Injection (SQL, Command, etc.)**
  - [ ] Use parameterized queries, prepared statements, or ORMs.
  - [ ] Implement strict input validation and output encoding.

- [ ] **A04: Insecure Design & Security Misconfigurations**
  - [ ] Remove default credentials, sample files, and unnecessary debugging features.
  - [ ] Ensure proper HTTP security headers are set (`Content-Security-Policy`, `X-Frame-Options`, `HSTS`).
