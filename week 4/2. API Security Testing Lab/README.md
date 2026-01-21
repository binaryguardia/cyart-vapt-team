# API Security Testing Lab

## Objective

Identify and exploit API vulnerabilities based on OWASP API Top 10.

Target Environment

Target Application: DVWA API

Target IP: 192.168.8.150

Tools Used

Burp Suite

Postman

sqlmap

Vulnerability Log
Test ID	Vulnerability	Severity	Target Endpoint
008	BOLA	Critical	/api/users
009	GraphQL Injection	High	/graphql
Manual Testing

Manipulated API tokens using Burp Suite to access unauthorized user data. GraphQL queries were fuzzed via Postman to extract sensitive schema information.

API Testing Summary (50 Words)

The API suffered from Broken Object Level Authorization and GraphQL injection flaws, allowing unauthorized data access. Poor access control and insufficient input validation were the root causes, highlighting the need for strict authorization checks and schema hardening.
