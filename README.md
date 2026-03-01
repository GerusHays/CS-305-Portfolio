# CS-305-Portfolio
# Artemis Financial Vulnerability Assessment

## Overview
This repository contains my vulnerability assessment and secure software analysis for Artemis Financial. The purpose of this project was to evaluate a financial web application for security vulnerabilities, identify risks, and recommend mitigation steps to improve the system’s security posture.

Artemis Financial is a financial services company that operates a web-based application handling sensitive customer and transaction data. Because financial applications process confidential information, security is critical to protect customer privacy, prevent fraud, and maintain trust.

This artifact demonstrates my ability to perform manual code review, run static security analysis tools, identify vulnerabilities, and implement secure software practices.

---

## Client Summary and Security Requirements

**Client:** Artemis Financial  
**Application Type:** Web-based financial services platform  

The company required secure communications and protection of sensitive financial data. Because the system processes customer and transaction information, it must prevent unauthorized access, protect data in transit, and reduce exposure to common web-based attacks.

Key security requirements included:

- Protecting sensitive financial data
- Preventing injection and cross-site scripting attacks
- Securing APIs and client-server communication
- Maintaining secure and updated dependencies
- Enforcing encryption and secure communication protocols
- Preventing unauthorized system access

Failure to secure the system could result in financial loss, legal consequences, and reputational damage.

---

## Security Vulnerabilities Identified

Through manual code review and static testing, I identified several security risks:

**Input validation issues**
- User input was accepted without validation or sanitization
- This created risk for injection attacks and cross-site scripting (XSS)

**Outdated and vulnerable dependencies**
- Spring Boot and other libraries were outdated
- Static analysis identified over 100 known vulnerabilities in dependencies

**Missing authentication and authorization**
- REST endpoints did not restrict access
- Any user could potentially access sensitive system functions

**Lack of HTTPS enforcement**
- No explicit configuration requiring encrypted communication

**Insufficient error handling and logging**
- Errors could expose internal system information
- Logging controls were not clearly defined

These vulnerabilities increased the attack surface and risk of data compromise.

---

## Static Testing and Security Tools Used

I used the following tool to identify known vulnerabilities:

**OWASP Dependency-Check (Maven Plugin)**

This tool scans project dependencies and compares them against the National Vulnerability Database (NVD) to identify known security issues.

The scan found:

- Multiple vulnerable dependencies
- High and critical severity CVEs
- Cryptographic and framework vulnerabilities
- Outdated libraries requiring upgrades

This reinforced the importance of maintaining secure and updated dependencies.

---

## Mitigation and Security Improvements

To address the identified vulnerabilities, I recommended the following actions:

- Implement strict input validation and output encoding
- Upgrade all dependencies to supported, secure versions
- Enforce HTTPS for all communications
- Add authentication and authorization controls
- Improve error handling to prevent information disclosure
- Separate development and production configurations
- Implement continuous vulnerability scanning

These steps significantly reduce risk and align the application with modern security best practices.

---

## Importance of Secure Coding

Secure coding is critical because vulnerabilities can expose sensitive data, allow unauthorized access, and compromise system integrity. Even small security flaws can be exploited if not addressed.

This project reinforced the importance of:

- Validating all user input
- Keeping dependencies updated
- Using secure communication protocols
- Following secure coding standards
- Integrating security testing into the development process

Security must be considered throughout the entire software lifecycle, not just after development.

---

## How I Verified Secure and Functional Code

After identifying vulnerabilities and implementing mitigation steps, I verified the application by:

- Running dependency-check scans to confirm vulnerabilities were resolved
- Reviewing code to ensure secure input handling
- Confirming updated dependencies compiled and ran correctly
- Ensuring the application still functioned as expected after changes

This helped ensure security improvements did not break system functionality.

---

## Tools and Practices Used

Tools:

- OWASP Dependency-Check
- Maven build system
- Static vulnerability scanning tools

Practices:

- Manual code review
- Secure coding principles
- Dependency management
- Vulnerability mitigation planning

These tools and practices are directly applicable to real-world secure software development.

---

## Skills Demonstrated

- Software vulnerability assessment  
- Static application security testing (SAST)  
- Dependency vulnerability analysis  
- Secure coding practices  
- Risk assessment and mitigation planning  
- Secure software development lifecycle awareness  

---

## Portfolio Purpose

This artifact demonstrates my ability to identify and mitigate security vulnerabilities in a software system. These skills are critical for software engineering, systems engineering, and cybersecurity roles, especially when working with applications that process sensitive or mission-critical data.
