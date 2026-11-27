# MEDIROZAH HOSPITAL
## Web Application Security Assessment & Penetration Testing Report

### Project Information

| Category | Details |
|---|---|
| Project | Hospital Web Application Security Assessment |
| Target | medirozahospital.com |
| Platform | Kali Linux |
| Assessment Type | Web Application Security Assessment |
| Researcher | Adigun Olamide Precious |
| Training Organization | NETWORKWALKS |
| Batch | B084 (Batch 84) |
| Field | Cybersecurity |
| Date | November 2026 |
| Status | In Progress |

---

## 1. Executive Summary

This project focuses on assessing the security of the MediRozah Hospital web application, identifying potential vulnerabilities, examining publicly accessible information, and evaluating the security of sensitive document handling.

The assessment applies standard cybersecurity tools and methodologies within the scope of the authorized testing environment.

The primary objective is to identify security weaknesses and provide recommendations to improve the confidentiality, integrity, and availability of the hospital's information systems.

## 2. Scope and Methodology

The assessment covers:

- Publicly accessible website information.
- Web server configuration.
- DNS information.
- Login page security observations.
- PDF document properties and metadata.
- Potential exposure of sensitive information.
- Security recommendations.

### Tools Used

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing environment |
| Nmap | Network and service discovery |
| WHOIS | Domain registration information |
| DIG | DNS information gathering |
| cURL | HTTP header inspection |
| ExifTool | PDF metadata examination |
| PDFinfo | PDF document properties |
| Firefox/Chrome | Website inspection |
| Wireshark | Network traffic analysis |

## 3. Assessment Activities

### M1 – Reconnaissance and Information Gathering

Activities performed:

- Identified the target domain.
- Examined DNS records.
- Retrieved MX records using DIG.
- Inspected HTTP response headers using cURL.
- Identified publicly accessible login pages.

**Observed Result:**

The staff login endpoint returned an HTTP 200 response during initial inspection.

**Command Used:**

```bash
curl -I https://medirozahospital.com/staff/login.php
```

This confirmed that the endpoint responded to an HTTP request. It does not independently establish whether authentication is vulnerable.

### M2 – Vulnerability Assessment

This phase focuses on identifying potential weaknesses in the web application.

Areas examined or planned for examination:

- Authentication mechanisms.
- Input validation.
- SQL injection exposure.
- Access control.
- HTTP security headers.
- Document access controls.

All testing must remain within the explicitly authorized scope.

### M3 – Critical Data Exposure

This phase examines recovered documents and their metadata.

Activities:

- Identify authorized assessment documents.
- Examine PDF document properties.
- Inspect metadata using ExifTool.
- Review document accessibility and protection.
- Identify any documented exposure of sensitive information.

**Data Protection Note:** Real patient and employee information must not be published in this report or uploaded to GitHub.

### M4 – Professional Reporting

The final report follows this structure:

1. Executive Summary
2. Scope and Methodology
3. Findings and Proof of Exploitation
4. Risk Rating
5. Recommendations and Remediation

## 4. Risk Rating

| Severity | Description |
|---|---|
| Critical | Vulnerability could result in severe system compromise. |
| High | Significant security weakness with serious consequences. |
| Medium | Vulnerability with moderate security impact. |
| Low | Limited security impact. |
| Informational | Observation that does not establish a vulnerability. |

No vulnerability should receive a severity rating without supporting evidence.

## 5. Recommendations and Remediation

Recommended security improvements include:

- Implement strong authentication mechanisms.
- Use parameterized SQL queries.
- Enforce role-based access control.
- Restrict access to sensitive PDF documents.
- Configure appropriate HTTP security headers.
- Encrypt sensitive information.
- Monitor authentication attempts.
- Conduct regular security assessments.

## 6. Conclusion

This assessment provides practical experience in web application security testing, reconnaissance, vulnerability assessment, document metadata analysis, and professional security reporting.

The project demonstrates the importance of identifying security weaknesses before they can be exploited and protecting sensitive information from unauthorized access.

**Project Status:** In Progress.

---

## Author Information

**Researcher:** Adigun Olamide Precious  
**Training Organization:** NETWORKWALKS  
**Training Batch:** B084 (Batch 84)  
**Field:** Cybersecurity  

*Documenting my cybersecurity learning journey through practical security assessment, technical investigation, and professional reporting.*
