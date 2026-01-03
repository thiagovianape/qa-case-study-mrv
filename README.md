# qa-case-study-mrv
Exploratory QA analysis of a public corporate website
# QA Case Study – Public Website Analysis (MRV)

## Objective
This repository documents a Quality Assurance exploratory analysis conducted on a public corporate website.
The goal is to practice QA skills by identifying technical warnings, integration issues, and potential improvements.

## Scope
- Public homepage
- Browser console analysis
- SEO and analytics-related observations
- No access to proprietary source code

## Methodology
- Manual exploratory testing
- Desktop browser (Chrome)
- Publicly observable behavior only

## Findings (Initial)

### 1. Malformed JSON-LD (Organization Schema)
- Description: Invalid JSON structure detected in structured data.
- Impact: SEO tools and analytics platforms may ignore the data.
- Severity: Medium
- Type: Technical / SEO

### 2. reCAPTCHA callback warning
- Description: reCAPTCHA script attempts to call a non-existent callback function.
- Impact: Potential risk in form validation under certain conditions.
- Severity: Medium
- Type: Integration warning

## Disclaimer
This project is for educational purposes only.
All observations are based on publicly accessible information.
No proprietary or confidential data is included.
