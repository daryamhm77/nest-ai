# Recipe: File Upload
1. Stream uploads (no full buffer in memory); cap size + validate MIME + extension.
2. Scan (AV hook) before persisting; store via a `StoragePort` (S3/MinIO adapter).
3. Persist metadata row; return a signed, time-limited URL for download.
4. Never trust client-provided filenames; generate keys server-side (tenant-scoped).
