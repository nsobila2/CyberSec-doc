# Cybersecurity Incident Report: Network Traffic Analysis
# Cybersecurity Incident Report: Network Traffic Analysis  
## Scenario  

Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location, which serves as their main office, a storefront, and warehouse for their products. However, Botium Toy’s online presence has grown, attracting customers in the U.S. and abroad. As a result, their information technology (IT) department is under increasing pressure to support their online market worldwide.  

The manager of the IT department has decided that an internal IT audit needs to be conducted. She's worried about maintaining compliance and business operations as the company grows without a clear plan. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets.  

The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).  

The IT manager starts by implementing the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), establishing an audit scope and goals, listing assets currently managed by the IT department, and completing a risk assessment.  

The goal of the audit is to provide an overview of the risks and/or fines that the company might experience due to the current state of their security posture.  

**Your task:** Review the IT manager’s scope, goals, and risk assessment report. Then, perform an internal audit by completing a controls and compliance checklist.  
## Audit Scope and Goals  

The IT manager at Botium Toys has defined the following scope and goals for the internal IT audit:  

### Scope  
- Review current IT infrastructure, including servers, networks, and applications.  
- Assess security controls in place for protecting sensitive customer and business data.  
- Evaluate compliance with regulations such as PCI DSS (for online payments) and GDPR (for E.U. customers).  
- Identify risks, threats, and vulnerabilities that may affect critical assets.  

### Goals  
- Ensure that security practices align with the NIST Cybersecurity Framework (CSF).  
- Provide recommendations for strengthening security posture.  
- Reduce the likelihood of data breaches or system downtime.  
- Support the company’s growth while maintaining compliance and trust with customers.  
## IT Assets List  
## IT Assets List  

The following assets are currently managed by the IT department:  

- **Servers**: Host customer data, website, and applications.  
- **Workstations**: Computers used by employees for daily business operations.  
- **Network devices**: Routers, switches, and firewalls that manage internal and external traffic.  
- **Payment processing systems**: Systems used for handling credit card and online payments.  
- **Customer data**: Personally Identifiable Information (PII) and payment details.  
- **Inventory management system**: Tracks products, orders, and stock.  
- **Email and communication tools**: Used for internal and external communication.  
## Risk Assessment  

| Risk Area                  | Description                                                      | Likelihood | Impact  |
|----------------------------|------------------------------------------------------------------|------------|---------|
| Customer Data Protection   | Risk of GDPR fines if E.U. customer data is not properly secured | Medium     | High    |
| Payment Processing         | Risk of PCI DSS non-compliance during online transactions       | Medium     | High    |
| Network Security           | Weak monitoring could allow unauthorized access                 | High       | High    |
| Business Continuity        | No formal incident response plan in place                        | Medium     | Medium  |
| Employee Awareness         | Lack of cybersecurity training could lead to phishing attacks   | High       | Medium  |
## Controls & Compliance Checklist  

| Control Area      | Compliance Standard | Status             | Notes                                     |
|------------------|------------------|------------------|-------------------------------------------|
| Access Control    | NIST CSF / PCI DSS | 🔴 Needs Improvement | No multi-factor authentication on POS   |
| Data Protection   | GDPR / PCI DSS    | 🟡 Partial         | Encryption in place, EU-specific gaps    |
| Network Monitoring| NIST CSF          | 🔴 Needs Improvement | No SIEM or IDS/IPS                        |
| Incident Response | NIST CSF          | 🔴 Not Implemented | No documented plan                        |
| Payment Security  | PCI DSS           | 🟡 Partial         | Processor compliant, internal controls weak |
| Employee Training | NIST CSF          | 🔴 Not Implemented | No cybersecurity awareness program       |
## Findings & Recommendations  

### Findings
- Current controls are insufficient to support secure global expansion.  
- Lack of an incident response plan and employee training increases risk of breaches.  
- Compliance gaps with GDPR and PCI DSS pose potential fines and legal issues.  
- Network monitoring is inadequate to detect intrusions or suspicious activity.  

### Recommendations
1. Implement multi-factor authentication (MFA) for POS systems and employee accounts.  
2. Deploy intrusion detection/prevention systems (IDS/IPS) or SIEM for network monitoring.  
3. Establish a formal Incident Response Plan with clear roles and procedures.  
4. Conduct regular employee cybersecurity training (phishing, password hygiene, etc.).  
5. Update Data Protection Policies to comply fully with GDPR for E.U. customers.  
## Conclusion  

Botium Toys is at moderate to high risk due to compliance gaps and limited security controls.  
Immediate focus should be placed on:  

- Strengthening data protection measures, especially for E.U. customer data.  
- Improving network monitoring and security infrastructure.  
- Implementing an incident response plan and employee cybersecurity training.  
- Ensuring compliance with PCI DSS and GDPR regulations.  

By addressing these areas, Botium Toys can reduce the risk of data breaches, avoid fines, and support safe business growth.
