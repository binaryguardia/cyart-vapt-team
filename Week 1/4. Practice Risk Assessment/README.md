# Risk Assessment and Prioritization

After documenting vulnerabilities, risk assessment was performed to understand the real-world impact and prioritize remediation efforts.

## Objective
- Evaluate the severity of identified vulnerabilities
- Prioritize risks based on likelihood and impact

## Tools Used
- **CVSS Calculator (v3.1 / v4.0)**
- **3x3 Risk Matrix (Likelihood vs Impact)**

---

## Step 1: CVSS Scoring

Each vulnerability was scored using the CVSS calculator to determine its severity.

### Process
1. Identify vulnerability details from scan results:
   - Attack Vector
   - Attack Complexity
   - Privileges Required
   - User Interaction
   - Impact on Confidentiality, Integrity, Availability

2. Enter values into the CVSS Calculator.

3. Record the generated:
   - Base Score
   - Severity Level  
     - Low (0.1 – 3.9)  
     - Medium (4.0 – 6.9)  
     - High (7.0 – 8.9)  
     - Critical (9.0 – 10.0)

### Example
- Vulnerability: Outdated Apache Tomcat  
- CVSS Score: 8.1  
- Severity: High

---

## Step 2: Risk Likelihood Assessment

Likelihood represents how easily the vulnerability can be exploited.

### Criteria
- **Low** – Requires special access or complex exploitation
- **Medium** – Exploitable with some effort
- **High** – Easily exploitable, public exploit available

Likelihood was assigned based on:
- Exploit availability
- Network exposure
- Authentication requirements

---

## Step 3: Impact Assessment

Impact measures the potential damage if the vulnerability is exploited.

### Criteria
- **Low** – Minimal service disruption
- **Medium** – Partial data exposure or service impact
- **High** – Data breach, system compromise, or service downtime

Impact was evaluated based on:
- Data sensitivity
- System criticality
- Business or operational effect

---

## Step 4: 3x3 Risk Matrix

A 3x3 risk matrix was used to prioritize vulnerabilities.

| Likelihood \ Impact | Low | Medium | High |
|---------------------|-----|--------|------|
| Low                 | Low | Low    | Medium |
| Medium              | Low | Medium | High |
| High                | Medium | High | Critical |

---

## Step 5: Risk Prioritization

Final risk level was determined by mapping:
- CVSS Severity
- Likelihood
- Impact

### Priority Order
1. **Critical**
2. **High**
3. **Medium**
4. **Low**

---

## Outcome
- High-risk vulnerabilities were prioritized for immediate remediation
- Medium-risk issues were scheduled for mitigation
- Low-risk findings were documented for monitoring

This process improves decision-making and strengthens overall security posture.

