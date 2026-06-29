# CSRF

- Pure token-bearer APIs (Authorization header) are not CSRF-prone — prefer this.
- If using cookie auth, require `SameSite` cookies + a CSRF token (double submit / synchronizer).
- State-changing requests must be POST/PUT/PATCH/DELETE, never GET.
- Validate `Origin`/`Referer` for cookie-authenticated mutations.
