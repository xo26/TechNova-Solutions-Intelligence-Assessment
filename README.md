# OSINT Case Study - TechNova Solutions Intelligence Assessment

![OSINT Case Study](OSINT%20Case%20Study%20-%20TechNova%20Solutions%20(Enhanced).png)

---

Report Overview

| **Detail** | **Information** |
|------------|-----------------|
| **Author** | Astral |
| **Date** | February 6, 2026 |
| **Target Type** | Corporate Intelligence (Open Sources Only) |
| **Engagement** | Open Source Intelligence (OSINT) Assessment |
| **Methodology** | DNS Reconnaissance → Infrastructure Analysis → Public Records Research → Security Assessment |

> **CONFIDENTIAL - OPEN SOURCES ONLY**  
> All information gathered exclusively from publicly available open sources per OSINT best practices.

---

Executive Summary

This OSINT case study presents a comprehensive intelligence assessment of TechNova Solutions and TechNova Imaging Systems, conducted entirely through publicly available open sources. The assessment includes infrastructure analysis, technology stack identification, leadership mapping, organizational structure analysis, and security assessment of the primary website.

---

Methodology

Open Source Intelligence (OSINT) Methods Used:

1. **DNS Reconnaissance**
   - Subdomain enumeration
   - Public DNS record analysis
   - IP address and ASN identification

2. **Public Records Research**
   - WHOIS data analysis
   - Public domain registration records
   - Publicly accessible company information

3. **Professional Network Analysis**
   - Public LinkedIn profile research
   - Public company pages
   - Professional network mapping

4. **Infrastructure Analysis**
   - Public SSL certificate analysis
   - Public hosting provider identification
   - Technology stack identification from public headers

5. **Public Website Analysis**
   - Publicly accessible website content
   - Public documentation review
   - Public API endpoint discovery

6. **Security Assessment**
   - OWASP PTK automated security scanning
   - Technology stack fingerprinting
   - Security headers analysis

---

Key Findings

Infrastructure Exposure

During the reconnaissance phase, I identified several publicly accessible subdomains and infrastructure components. The main findings include four subdomains that are accessible without authentication:

- **demo.technovasolutions.io** (IP: 49.13.52.164) - Demo/Testing environment
- **nms.technovasolutions.io** (IP: 49.13.52.164) - Network Management System
- **odoo17.technovasolutions.io** (IP: 5.75.231.60) - Odoo 17 ERP system
- **wap.technovasolutions.io** (IP: 49.13.128.107) - Web Application Portal

The hosting infrastructure is managed by Hetzner Online GmbH in Germany (ASN: 24940). The IP ranges identified are 49.13.0.0/16 and 5.75.128.0/17, both belonging to HETZNER-AS. I was able to identify an Odoo 17 ERP system running on one of the subdomains, which is a Python-based enterprise resource planning platform used for CRM, accounting, inventory management, and human resources.

This represents a medium-high risk as internal systems are exposed to public enumeration. The demo environment being publicly accessible is particularly concerning as it may contain test data or configuration information that could be useful for attackers.

Organizational Structure

TechNova operates as a dual-entity structure with TechNova Imaging Systems (P) Ltd. as the parent manufacturing company and TechNova Solutions as the IT/services division. The parent company is reported to have 1,000-4,999 employees with revenue in the $250-499 Million range.

The leadership team is relatively small, with Amit Khurana serving as CEO/COO (promoted from COO between 2022-2026) and Piyush Kapadia holding the CFO/CTO position. This centralized structure suggests tight control over decision-making processes. The dual CFO/CTO role is unusual and may indicate cost optimization or a lean organizational structure.

Key Personnel Identified:
- Amit Khurana - CEO/COO, over 18 years at the company, MBA, IIM Ahmedabad graduate
- Piyush Kapadia - CFO/CTO, handles both finance and IT operations
- Jeniffer K - DevOps Engineer, works at both TechNova Solutions and NXWEB (potential partner)

The recent promotion of the CEO from COO suggests internal growth and possibly an expansion phase for the company.

Digital Assets

The company maintains three primary domains: technovaworld.com, technovaindia.com, and technovasolutions.io. I identified a structured email system with department-based addresses including:

- sales@technovasolutions.io
- support@technovasolutions.io
- devops@technovasolutions.io
- a.khurana@technovaworld.com (CEO)
- piyush.kapadia@technovaindia.com (CFO/CTO)

There's also evidence of international operations, with a Qatar phone number (+974 7123 3234) associated with some employees, suggesting Middle East market presence or regional operations.

Corporate Email Infrastructure

The email structure follows a standard corporate format (department@domain), indicating an organized communication system. All emails are associated with the three main domains, suggesting a unified digital infrastructure across the different business units.

---

Security Assessment - www.technovaworld.com

Technology Stack Identified

| Technology | Version | Category |
|------------|---------|----------|
| Google Font API | - | Font scripts |
| Bootstrap | 3.4.1 | UI frameworks |
| jQuery | 3.7.1 | JavaScript libraries |
| jQuery UI | 1.14.1 | JavaScript libraries |
| HSTS | - | Security |
| nopCommerce | - | E-commerce |
| Zoho CRM | - | CRM |
| Microsoft ASP.NET | - | Web frameworks |
| Google Analytics | GA4 | Analytics |
| Zoho PageSense | - | A/B Testing, Personalisation |
| FortiWeb (Fortinet) | - | WAF |

Security Headers Analysis

The security headers analysis revealed several areas that could be improved. The Content Security Policy (CSP) allows inline/eval or wildcards in script/style, which reduces its effectiveness. The CSP 'frame-ancestors' directive is either missing or configured too broadly. The HSTS implementation has a max-age that's too low or is missing the includeSubDomains flag. Additionally, some legacy security headers like X-Frame-Options and X-XSS-Protection are still in use, though these are being phased out in favor of CSP.

Overall, this represents a medium risk level. The security headers configuration needs improvement, particularly around implementing stricter CSP policies and updating to modern security header standards.

Web Application Framework
- **Primary Framework:** Microsoft ASP.NET
- **E-commerce Platform:** nopCommerce
- **WAF:** FortiWeb (Fortinet) - Web Application Firewall detected
- **CRM Integration:** Zoho CRM

Third-Party Services
- **Analytics:** Google Analytics GA4
- **A/B Testing:** Zoho PageSense
- **CRM:** Zoho CRM
- **CDN/Fonts:** Google Font API

Security Posture

The website shows evidence of active security measures with FortiWeb (Fortinet) Web Application Firewall detected. This indicates the company is investing in security infrastructure. However, the security headers configuration needs improvement. HSTS is enabled but the configuration could be strengthened, and some legacy security headers are still in use.

The presence of a WAF suggests the company is aware of security threats and has taken steps to protect their web applications. However, the security headers analysis shows room for improvement in implementing modern security standards.

Risk Assessment Summary

- **Infrastructure Exposure:** Medium-High risk due to publicly accessible subdomains including demo environments and internal systems
- **Security Headers:** Medium risk - configuration needs improvement but WAF protection is present
- **Technology Stack:** Modern stack with some legacy components (Bootstrap 3.4.1, older jQuery versions)
- **Organizational Structure:** Centralized leadership suggests efficient decision-making but also potential single points of failure

---

Data Sources

All information in this report was gathered exclusively from:
- Public DNS records
- Publicly accessible websites
- Public LinkedIn profiles
- Public domain registration data
- Public infrastructure analysis
- OWASP PTK automated security scanning (public website analysis)

**No closed sources, breach databases, or proprietary data were used in this assessment.**

---

Files

- **[OSINT Case Study - TechNova Solutions (Enhanced).pdf](OSINT%20Case%20Study%20-%20TechNova%20Solutions%20(Enhanced).pdf)** - Full PDF report
- **[OSINT Case Study - TechNova Solutions (Enhanced).png](OSINT%20Case%20Study%20-%20TechNova%20Solutions%20(Enhanced).png)** - Preview image

---

> **CONFIDENTIAL - OPEN SOURCES ONLY**  
> All information in this report gathered exclusively from publicly available open sources. No closed sources, breach databases, or proprietary data were used.

---

Tags

`#OSINT` `#CaseStudy` `#Intelligence` `#TechNova` `#OpenSources` `#SecurityAssessment` `#PTK`
