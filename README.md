# API Security Risk Analysis – JSONPlaceholder

## Overview
This project presents a comprehensive API Security Risk Analysis conducted on the JSONPlaceholder REST API. The objective of this assessment was to identify common API security vulnerabilities and evaluate the risks associated with insecure API design.

The analysis simulates a real-world security assessment using industry-standard tools and methodologies. Findings are aligned with established API security principles, including those outlined by the OWASP API Security Top 10.

## Objectives
- Analyse publicly accessible API endpoints  
- Identify potential security vulnerabilities  
- Evaluate risks associated with API misconfigurations  
- Provide remediation recommendations based on best practices  

## Tools and Technologies
- Postman – API testing and request analysis  
- Google Chrome – Response verification  
- JSONPlaceholder API – Target system for testing
  
## Methodology
The assessment followed a black-box testing approach, simulating an external attacker with no prior authentication or system access.

Key steps included:
- Sending HTTP GET requests to multiple endpoints  
- Analysing response data, headers, and status codes  
- Testing endpoint accessibility without authentication  
- Manipulating endpoint parameters (e.g., user IDs)  
- Capturing evidence through screenshots  

## Key Findings

### 1. Unauthenticated API Access
Multiple API endpoints were accessible without authentication, allowing unrestricted access to data.

Risk Level: Medium  

### 2. Insecure Direct Object Reference (IDOR)
User-specific data could be accessed by modifying object identifiers within the endpoint URL, with no authorization checks in place.

Risk Level: High  

### 3. Excessive Data Exposure
The API returned more data than necessary, including user details that could be considered sensitive in a real-world context.

Risk Level: Medium  

## Recommendations
- Implement authentication mechanisms such as API keys, OAuth, or JWT  
- Enforce proper authorization controls to restrict access to resources  
- Apply data minimization principles to limit exposed information  
- Introduce rate limiting and input validation to improve resilience  

## Evidence
All findings are supported by screenshots located in the `/screenshots` directory, demonstrating API responses and observed behaviours.

## Project Structure
```
API-Security-Task3/
│
├── report.pdf
├── screenshots/
│   ├── step1_users_endpoint.png
│   ├── step2_posts_endpoint.png
│   ├── step2_comments_endpoint.png
│   ├── step3_user_id_access.png
│   ├── step3_query_filter.png
```

## Key Learning Outcomes
- Understanding of API security risks and vulnerabilities  
- Practical experience with API testing tools  
- Ability to identify and document security weaknesses  
- Application of API security best practices  

## Disclaimer
This project was conducted for educational purposes only. The JSONPlaceholder API is intentionally unsecured and designed for testing and learning. No real systems were harmed or exploited during this assessment.


## Author
Seadimo Bugqwangu  
Cybersecurity Enthusiast | Junior Software Engineer
