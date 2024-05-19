# Technical Report: Ethical Hacking Assessment

**Date:** May 18, 2024  
**Client:** Birthing Home Website
**Prepared by:** Edlan Rey and Dominique Julienne

## Executive Summary:
This ethical hacking assessment aimed to identify and address security vulnerabilities within Birthing Home's IT infrastructure. The assessment uncovered several critical, high, and medium-risk issues that could potentially be exploited by malicious actors. The findings and corresponding recommendations are provided to enhance the security posture of the client's web applications and systems.

## Findings:

1. **SQL Injection (Critical):**
   - SQL injection vulnerabilities were found in the login and search functionalities. This allows attackers to execute arbitrary SQL commands, potentially leading to data breaches and unauthorized access to sensitive information.

2. **Cross-Site Scripting (XSS) (High):**
   - Multiple instances of reflected XSS were identified, enabling attackers to inject malicious scripts into web pages viewed by other users. This could result in session hijacking, defacement, or phishing attacks.

3. **Outdated Software (High):**
   - Several components of the web application, including the web server and CMS, are running outdated versions with known vulnerabilities. This increases the risk of exploitation through publicly available exploits.

4. **Weak Password Policy (High):**
   - The current password policy lacks complexity requirements and enforcement of periodic changes. This makes it easier for attackers to perform brute-force or dictionary attacks to compromise user accounts.

5. **Missing Security Headers (Medium):**
   - Important security headers such as Content Security Policy (CSP), X-Content-Type-Options, and X-Frame-Options are missing. This leaves the website vulnerable to a range of attacks, including clickjacking and MIME type sniffing.

6. **Unrestricted File Upload (Medium):**
   - The file upload functionality does not properly validate or sanitize uploaded files. This could allow attackers to upload and execute malicious files, leading to server compromise.

7. **Sensitive Data Exposure (Medium):**
   - Sensitive information, including error messages and stack traces, is being exposed in the application's responses. This provides attackers with valuable information for exploiting vulnerabilities.

8. **Insecure Direct Object References (IDOR) (Medium):**
   - IDOR vulnerabilities were identified, where unauthorized users can access or modify data by manipulating object references in the URL. This can lead to unauthorized data access and manipulation.

9. **Insecure Deserialization (High):**
   - The application deserializes untrusted data without proper validation. This vulnerability can be exploited to execute arbitrary code, leading to full system compromise.

10. **Cross-Site Request Forgery (CSRF) (Medium):**
    - CSRF vulnerabilities exist, allowing attackers to perform actions on behalf of authenticated users without their consent. This can result in unauthorized transactions or changes to user data.

## Recommendations:

1. **SQL Injection:** 
   - Implement parameterized queries and prepared statements to prevent SQL injection. Conduct a thorough code review and use input validation techniques.

2. **Cross-Site Scripting (XSS):**
   - Sanitize and encode user inputs to prevent XSS attacks. Implement Content Security Policy (CSP) to mitigate the impact of XSS vulnerabilities.

3. **Outdated Software:** 
   - Regularly update and patch all software components. Implement a patch management process to ensure timely updates.

4. **Weak Password Policy:** 
   - Enforce a strong password policy requiring complex passwords and regular changes. Implement multi-factor authentication (MFA) for added security.

5. **Missing Security Headers:** 
   - Configure the web server to include necessary security headers like Content Security Policy (CSP), X-Content-Type-Options, X-Frame-Options, and others to enhance security.

6. **Unrestricted File Upload:** 
   - Validate and sanitize all uploaded files. Restrict the types of files that can be uploaded and implement virus scanning for uploaded files.

7. **Sensitive Data Exposure:** 
   - Avoid displaying detailed error messages and stack traces to users. Configure error handling to log detailed errors internally and show generic messages to users.

8. **Insecure Direct Object References (IDOR):** 
   - Implement access controls and validate user permissions before allowing access to objects. Use indirect references to objects wherever possible.

9. **Insecure Deserialization:** 
   - Avoid deserializing untrusted data. Use secure deserialization libraries and validate data before deserializing.

10. **Cross-Site Request Forgery (CSRF):** 
    - Implement anti-CSRF tokens in forms and validate them on the server side. Ensure that state-changing operations are protected against CSRF.

## Conclusion:
The ethical hacking assessment identified several critical, high, and medium-risk vulnerabilities in Birthing Home’s IT infrastructure. Immediate remediation actions are necessary to address these issues and enhance the overall security posture. Implementing the recommended measures will help protect the website from potential attacks and secure sensitive data.

## Disclaimer:
This report is based on the findings from a specific point in time and may not reflect current vulnerabilities or risks. Regular security assessments and updates are recommended to maintain a strong security posture.

## Signature:

![Edlan Rey's Signature](images/edlan-rey-signature.png)  
**Edlan Rey**

![Dominique Julienne's Signature](images/dominique-julienne-signature.png)  
**Dominique Julienne**
