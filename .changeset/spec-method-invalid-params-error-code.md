---
'@modelcontextprotocol/core': patch
---

Return `-32602 InvalidParams` instead of `-32603 InternalError` when a spec-method request handler receives schema-invalid params. The dispatch-time parse failure previously escaped as a raw error and was wrapped as an internal error, telling callers the server broke rather than that their params were wrong.
