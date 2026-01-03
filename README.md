# qa-case-study-mrv
Exploratory QA analysis of a public corporate website
# QA Case Study – Public Website Analysis (MRV)

## Objective
This repository documents a Quality Assurance exploratory analysis conducted on a public corporate website (https://www.mrv.com.br).  
The goal is to practice QA skills by identifying technical warnings, integration issues, and potential improvements observable from the client side.

---

## Scope
This QA study focuses on:
- Homepage and publicly accessible pages
- Browser console analysis
- Third-party integrations (reCAPTCHA, Meta Pixel)
- Structured data validation (JSON-LD / Schema.org)
- SEO/Analytics impact

> No access to proprietary source code, backend systems, or private assets was used.

---

## Methodology
The investigation was performed via:
1. Manual browsing in desktop browser (Chrome)
2. Opening DevTools (F12) → Console
3. Observing warnings and data structures
4. Verifying behavior with simple user flows

Tools used:
- Chrome DevTools  
- Browser console  
- Visual Studio Code (Markdown editing)

---

## Findings

### Malformed JSON-LD (Organization Schema)
**Description:**  
The webpage contains JSON-LD structured data block that is not well-formed, causing parsing errors.

**Error observed:**  

**Root cause:**  
The `telephone` property is located inside the `sameAs` array, which is syntactically invalid.

**Impact:**
- SEO tools (Google) may ignore structured data
- Analytics and social pixel (Meta/Facebook) cannot extract organization info
- Potential loss of rich results and data consistency

**Severity:** Medium  
**Type:** Technical / SEO / Structured Data

---

### reCAPTCHA callback warning
**Description:**  
Browser console displays warning when loading Google reCAPTCHA:

**Root cause:**  
The reCAPTCHA script references a non-existent callback function in the global scope.

**Impact:**
- May affect form validation under some conditions
- Does not block immediate user interaction
- Requires developer attention in scripts

**Severity:** Medium  
**Type:** Integration / Script loading

---

## Conclusion
This case study highlights technical warnings observable in the browser console that may impact SEO, analytics, and third-party integrations.  
Although no direct user-facing malfunction was found on the homepage, these issues are worth addressing from a quality standpoint.

---

## Disclaimer
This project is for educational and portfolio purposes only.  
All data and artifacts are based on publicly accessible browser behavior.
