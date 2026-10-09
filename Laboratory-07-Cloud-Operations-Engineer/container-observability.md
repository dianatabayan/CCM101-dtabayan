# Container Observability

## Checkpoint 4: Application Logging

**404 error log line:**

```
172.17.0.1 - - [09/Oct/2026:13:48:38 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

**Why application logs are vital:**
Application logs record exactly what happened and when, such as which page was requested and whether it succeeded or failed, so an engineer can trace the cause of an error after the fact. Without them, troubleshooting a broken service would mean guessing instead of reading the evidence.
