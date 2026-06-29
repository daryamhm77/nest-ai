# XSS

- APIs return JSON only; set `Content-Type: application/json` and never reflect raw HTML.
- Escape/encode any user content rendered server-side.
- Set security headers via Helmet: CSP, `X-Content-Type-Options: nosniff`.
- Sanitize rich-text inputs server-side with an allowlist.
- Cookies holding tokens are `HttpOnly` so script cannot read them.
