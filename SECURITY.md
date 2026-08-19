# Security Policy for CareerShield AI

## Data Handling & Protection
CareerShield AI takes user privacy seriously. As an application interacting with sensitive job seeker documents (offer letters, resumes, recruiter emails), we enforce a strict data handling policy:

1. **Zero-Persistence:** User-uploaded documents and text inputs are processed entirely in memory and immediately discarded after analysis. We do not store raw PII (Personally Identifiable Information) in our database.
2. **PII Sanitization:** Before any text or document is sent to the Google Gemini API for analysis, our internal sanitization engine scrubs explicit identifiers (names, personal email addresses, phone numbers).
3. **Third-Party API Security:** Communication with Google's API is secured via encrypted HTTPS payloads. API keys are strictly managed via environment variables and are never exposed to the client-side frontend.
4. **Generative AI Constraints:** Strict JSON schema generation is enforced on the LLM to prevent prompt injection and data leakage.

## Reporting a Vulnerability
If you discover a security vulnerability within this project during the hackathon evaluation, please do not open a public issue. Email the team lead directly at [Insert Your Email Here] with the subject "SECURITY VULNERABILITY - CareerShield AI".
