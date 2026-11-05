# Secure Development Checklist

Name: Betty
Date: 4 November 2026

## 1. Pipeline map

| Stage | Security activity | Example tool | Gate (what blocks progress) |
| --- | --- | --- | --- |
| Plan | Write security requirements and assess risk | Checklist, gap analysis | Requirements approved |
| Design | Threat modelling | STRIDE | Top threats have countermeasures |
| Code | Scan while you type and peer review | SonarQube for IDE, Snyk IDE plugin | No hard-coded secrets, pull request reviewed |
| Build | SAST, SCA and secrets scan | Snyk, Dependency-Check | No new High or Critical findings |
| Test | Security tests and DAST | OWASP ZAP, penetration test | No open High findings |
| Deploy | Harden configuration and protect secrets | Security headers, secrets manager | Configuration checklist signed off |
| Operate | Monitor, patch and audit | Dependabot, logs, scheduled scans | Critical patches within agreed time |

## 2. My own additions (one more security activity for each stage)

- Plan:Plan budget and requirement needed
- Design:Decide what to build and how, including security needs.
- Code:Write the software and keep it in version control (GitHub).
- Build:Compile and package the code automatically (Jenkins).
- Test:Check that it works and is secure (Snyk, Dependency-Check).
- Deploy:Release it to a server or environment.
- Operate:Run it, monitor it, and fix problems, which feed back into plan

## 3. My pass or fail rules for three gates

1. Gate: Build. Rule: the build fails if Snyk reports any High or Critical issue.
2. Gate:
3. Gate:

## 4. SonarQube for IDE warnings I saw in app.js

-Web application technologies should not disclose version information (javascript:S5689)

solution: Proper input validation (by design) to prevent unauthorised data exposure.
 
## 5. snyk for IDE warnings i saw in app.js