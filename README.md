# QA Case Study – Public Website Analysis (MRV)

Exploratory Quality Assurance analysis of a public corporate website for learning and portfolio purposes.


---

## 🧠 Objective
This repository documents a Quality Assurance exploratory analysis conducted on a public corporate website (https://www.mrv.com.br).  
The goal is to practice QA skills by identifying technical warnings, integration issues, and potential improvements observable from the client side.

---

## 🔍 Scope
This QA study focuses on:
- Homepage and publicly accessible pages
- Browser console analysis
- Third-party integrations (reCAPTCHA, Meta Pixel)
- Structured data validation (JSON-LD / Schema.org)
- SEO and analytics impact

> No access to proprietary source code, backend systems, or private assets was used.

---

## 🧪 Methodology
The investigation was performed via:
- Manual exploratory testing
- Operating System: macOS
- Browser: Safari (Desktop)
- Observation of warnings and data structures
- Verification of behavior with simple user flows

Tools used:
- Safari Web Inspector  
- Browser console  

---

## 📌 Findings

### 1️⃣ Malformed JSON-LD (Organization Schema)

**Description:**  
The webpage contains a JSON-LD structured data block that is not well-formed, causing parsing errors in third-party tools.

**Error observed:**  
[Meta Pixel] - Unable to parse JSON-LD tag. Malformed JSON found

**Root cause:**  
The `telephone` property is incorrectly declared inside the `sameAs` array, which makes the JSON structure invalid.

**Impact:**
- SEO tools (Google) may ignore structured data
- Analytics and social platforms (Meta/Facebook) cannot extract organization information
- Potential loss of rich results and data consistency

**Severity:** Medium  
**Type:** Technical / SEO / Structured Data

---

### 2️⃣ reCAPTCHA Callback Warning

**Description:**  
A warning is displayed in the browser console during page load related to Google reCAPTCHA.

**Error observed:**  
reCAPTCHA couldn't find user-provided function: onloadcallback

**Root cause:**  
The reCAPTCHA script references a callback function that is not defined in the global scope.

**Impact:**
- Potential risk to form validation under specific conditions
- Does not block immediate user interaction
- Requires technical review of script loading order

**Severity:** Medium  
**Type:** Integration / Script Loading

---

## 🧾 Conclusion
This case study highlights technical warnings observable through browser console inspection that may impact SEO, analytics, and third-party integrations.  
Although no direct user-facing malfunction was identified on the homepage, these findings represent quality improvement opportunities from a technical perspective.

---

## ⚠️ Disclaimer
This project is for educational and portfolio purposes only.  
All observations are based on publicly accessible browser behavior.
