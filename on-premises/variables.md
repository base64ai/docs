# Base64 Ultimate Environment Variables

This document provides a comprehensive reference for all environment variables used in Base64 Ultimate on-premises deployment.

## Table of Contents

- [Api Service](#api-service)
  - [Admin](#api-admin)
  - [Branding](#api-branding)
  - [Database](#api-database)
  - [Elasticsearch](#api-elasticsearch)
  - [Email](#api-email)
  - [Integrations](#api-integrations)
  - [LDAP](#api-ldap)
  - [LLM](#api-llm)
  - [Logging](#api-logging)
  - [ML Services](#api-ml-services)
  - [Processing](#api-processing)
  - [Security](#api-security)
  - [Server](#api-server)
  - [Session](#api-session)
  - [Storage](#api-storage)
- [Sparrow Service](#sparrow-service)
  - [Logging](#sparrow-logging)
  - [Security](#sparrow-security)
  - [Server](#sparrow-server)
- [Toucan Service](#toucan-service)
  - [Logging](#toucan-logging)
  - [Security](#toucan-security)
  - [Server](#toucan-server)
- [Tomcat Service](#tomcat-service)
  - [Logging](#tomcat-logging)
  - [Security](#tomcat-security)
  - [Server](#tomcat-server)
- [Seagull Service](#seagull-service)
  - [Logging](#seagull-logging)
  - [Security](#seagull-security)
  - [Server](#seagull-server)
- [Pelican Service](#pelican-service)
  - [Logging](#pelican-logging)
  - [Security](#pelican-security)
  - [Server](#pelican-server)
- [Kiwi Service](#kiwi-service)
  - [Logging](#kiwi-logging)
  - [Security](#kiwi-security)
  - [Server](#kiwi-server)
- [Heron Service](#heron-service)
  - [Logging](#heron-logging)
  - [Security](#heron-security)
  - [Server](#heron-server)
- [Abbot Service](#abbot-service)
  - [Logging](#abbot-logging)
  - [Security](#abbot-security)
  - [Server](#abbot-server)
- [Merlin Service](#merlin-service)
  - [LLM](#merlin-llm)
  - [Logging](#merlin-logging)
  - [Processing](#merlin-processing)
  - [Security](#merlin-security)
  - [Server](#merlin-server)
- [Pheasant Service](#pheasant-service)
  - [Server](#pheasant-server)
- [Hawk Service](#hawk-service)
  - [Logging](#hawk-logging)
  - [Security](#hawk-security)
- [Vulture Service](#vulture-service)
  - [Logging](#vulture-logging)
  - [Security](#vulture-security)
- [Lark Service](#lark-service)
  - [Logging](#lark-logging)
  - [Security](#lark-security)
  - [Server](#lark-server)
- [Parrot Service](#parrot-service)
  - [Logging](#parrot-logging)
  - [Security](#parrot-security)
  - [Server](#parrot-server)
- [Crow Service](#crow-service)
  - [Logging](#crow-logging)
  - [Security](#crow-security)
  - [Server](#crow-server)

---

## Api Service

Main API server

### Api Admin

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_ADMIN_DOMAINS` | - | Comma-separated list of admin email domains, e.g., "example.com,acme.com" |
| `BASE64AI_ADMIN_EMAIL` | - | Email address for the admin user (on-premises), e.g., "admin@example.com" |
| `BASE64AI_ADMIN_FAMILY_NAME` | - | Last name for the admin user (on-premises), e.g., "Smith" |
| `BASE64AI_ADMIN_GIVEN_NAME` | - | First name for the admin user (on-premises), e.g., "John" |
| `BASE64AI_ADMIN_PASSWORD` | - | Password for the admin user (on-premises), e.g., "SecureP@ssw0rd!" |
| `BASE64AI_CREATE_ADMIN_USER` | `false` | Create admin user on startup (on-premises) Values: `true`, `false` |
| `BASE64AI_STATIC_USER_EMAIL` | - | Email for static user authentication (on-premises), e.g., "user@example.com" |
| `BASE64AI_STATIC_USER_FAMILY_NAME` | - | Last name for static user (on-premises), e.g., "Doe" |
| `BASE64AI_STATIC_USER_GIVEN_NAME` | - | First name for static user (on-premises), e.g., "Jane" |
| `BASE64AI_STATIC_USER_SECRET` | - | Password for static user authentication (on-premises), e.g., "UserP@ssw0rd!" |

### Api Branding

| Variable | Default | Description |
|----------|---------|-------------|
| `ON_PREM_TITLE` | - | Display title for on-premises deployment, e.g., "ACME Document AI" |

### Api Database

| Variable | Default | Description |
|----------|---------|-------------|
| `DATABASE_LOGGING_ENABLED` | `false` | Enable SQL query logging for debugging Values: `true`, `false` |
| `DATABASE_SERVER_DISABLED` | `false` | Disable the SQL database server feature Values: `true`, `false` |
| `DATABASE_SERVER_ENABLED` | `false` | Enable SQL database server for on-premises deployments Values: `true`, `false` |
| `DATABASE_SERVER_FLAVOR` | `sqlite` | Type of SQL database to use Values: `sqlite`, `postgres`, `mssql` |
| `DATABASE_SERVER_HOST` | `127.0.0.1` | Hostname of the SQL database server, e.g., "postgres.internal" or "10.0.0.5" |
| `DATABASE_SERVER_NAME` | - | Name of the SQL database, e.g., "base64api" |
| `DATABASE_SERVER_PASS` | - | Password for SQL database authentication, e.g., "db_secure_password" |
| `DATABASE_SERVER_PORT` | - | Port number of the SQL database server, e.g., "5432" for PostgreSQL, "1433" for MSSQL |
| `DATABASE_SERVER_SCHEMA` | - | Schema name for PostgreSQL database, e.g., "base64api" or "public" |
| `DATABASE_SERVER_STORAGE_PATH` | - | File path for SQLite database storage, e.g., "/data/base64.db" |
| `DATABASE_SERVER_USER` | - | Username for SQL database authentication, e.g., "base64_user" |
| `DISABLE_DATABASE_LOGS` | `false` | Disable database operation logging Values: `true`, `false` |

### Api Elasticsearch

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_ELASTIC_NUMBER_OF_SHARDS` | `1` | Number of shards for Elasticsearch indices, e.g., "1" for small deployments, "5" for large |
| `ELASTIC_SEARCH_API_KEY` | - | Elasticsearch Cloud API key (for cloud deployments), e.g., "dXNlcjpwYXNzd29yZA==" |
| `ELASTICSEARCH_API_KEY` | - | API key for Elasticsearch authentication, e.g., "VnVhQ2ZHY0JDZGJrUW0tZTVhT3g6dWkybHAyYXhUTm1zeWFr" |
| `ELASTICSEARCH_CA_CERT` | - | CA certificate for Elasticsearch TLS/SSL connections (PEM format string or file path) |
| `ELASTICSEARCH_NODE` | - | URL of the Elasticsearch node, e.g., "http://elasticsearch:9200" or "https://es.example.com:9243" |
| `ELASTICSEARCH_PASSWORD` | - | Password for Elasticsearch basic authentication, e.g., "elastic_password" |
| `ELASTICSEARCH_TLS_REJECT_UNAUTHORIZED` | `true` | Whether to reject unauthorized TLS certificates for Elasticsearch (set to "false" for self-signed certs) Values: `true`, `false` |
| `ELASTICSEARCH_USERNAME` | - | Username for Elasticsearch basic authentication, e.g., "elastic" |

### Api Email

| Variable | Default | Description |
|----------|---------|-------------|
| `SMTP_SERVER` | - | SMTP server URL for email notifications, e.g., "smtps://user:pass@smtp.example.com:465" |
| `SMTP_SERVER_DISABLED` | `false` | Disable SMTP server feature Values: `true`, `false` |

### Api Integrations

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_INTEGRATE_ADMIN_ACCOUNT_PASSWORD` | - | Admin account password for the integration server, e.g., "IntegrateP@ss123" |
| `BASE64AI_INTEGRATE_ADMIN_KEY` | - | Admin API key for the integration server, e.g., "n8n_admin_key_abc123" |
| `BASE64AI_INTEGRATE_COOKIE_NAME` | - | Cookie name for integration server session, e.g., "n8n.session" |
| `INTEGRATE_ADMIN_ACCOUNT` | - | Admin account email for the integration server, e.g., "admin@example.com" |
| `INTEGRATE_EXTERNAL_HOST_NAME` | - | External URL of the n8n integration server, e.g., "https://integrate.example.com" |
| `INTEGRATE_INTERNAL_HOST_NAME` | - | Internal URL of the n8n integration server, e.g., "http://n8n:5678" |
| `INTEGRATE_SERVER_DISABLED` | `false` | Disable the integration server feature Values: `true`, `false` |

### Api LDAP

| Variable | Default | Description |
|----------|---------|-------------|
| `LDAP_AUTHENTICATION_METHOD` | `full_dn` | LDAP authentication method, e.g., "user_principal_name" for Azure AD, "sam_account_name" for Active Directory Values: `full_dn`, `user_principal_name`, `sam_account_name` |
| `LDAP_BASE_DN` | - | Base DN for LDAP searches, e.g., "dc=base64,dc=ai" |
| `LDAP_CA` | - | CA certificate for LDAP server TLS connection. Accepts file path (e.g., "/etc/ssl/certs/ldap-ca.pem") or raw PEM content (e.g., "-----BEGIN CERTIFICATE-----...") |
| `LDAP_COMPANY_NAME_ATTRIBUTE` | `company` | LDAP attribute for user company name, e.g., "company" or "o" |
| `LDAP_EMAIL_ATTRIBUTE` | `mail` | LDAP attribute for user email address, e.g., "mail" or "userPrincipalName" |
| `LDAP_FAMILY_NAME_ATTRIBUTE` | `familyName` | LDAP attribute for user family name, e.g., "sn" or "familyName" |
| `LDAP_GIVEN_NAME_ATTRIBUTE` | `givenName` | LDAP attribute for user given name, e.g., "givenName" |
| `LDAP_GROUP_CLASS` | - | LDAP object class for groups, e.g., "group" for Active Directory or "groupOfNames" for OpenLDAP |
| `LDAP_GROUP_DNS` | - | Semicolon-separated list of group DNs for access control, e.g., "cn=Admins,ou=Permission_Groups,ou=groups,dc=base64,dc=ai;cn=Users,ou=Permission_Groups,ou=Groups,dc=base64,dc=ai" |
| `LDAP_GROUP_ID_ATTRIBUTE` | `objectGUID` | LDAP attribute for group ID, e.g., "objectGUID" for Active Directory or "cn" for OpenLDAP |
| `LDAP_GROUP_MAIL_ATTRIBUTE` | `mail` | LDAP attribute for group email, e.g., "mail" |
| `LDAP_GROUP_MEMBERSHIP_ATTRIBUTE` | `memberOf` | LDAP attribute for group membership on user objects, e.g., "memberOf" for Active Directory |
| `LDAP_GROUPS_ATTRIBUTE` | - | LDAP attribute for group member lookup, e.g., "member" for Active Directory |
| `LDAP_GROUPS_SEARCH_BASE` | - | Base DN for LDAP group searches, e.g., "ou=Groups,dc=base64,dc=ai" |
| `LDAP_LOGGING` | - | LDAP logging level for troubleshooting authentication issues Values: `debug`, `info`, `warn`, `error` |
| `LDAP_PHONE_NUMBER_ATTRIBUTE` | `telephoneNumber` | LDAP attribute for user phone number, e.g., "telephoneNumber" |
| `LDAP_SAM_ACCOUNT_PREFIX` | - | Prefix for SAM account names in LDAP (for sam_account_name auth method), e.g., "DOMAIN\\" or leave empty |
| `LDAP_SERVICE_ACCOUNT_DN` | - | DN for LDAP service account used for searches, e.g., "cn=appServiceAccount,ou=Service Accounts,dc=base64,dc=ai" |
| `LDAP_SERVICE_ACCOUNT_PASSWORD` | - | Password for LDAP service account |
| `LDAP_SERVICE_ENABLED` | `false` | Enable LDAP authentication service for on-premises deployments Values: `true`, `false` |
| `LDAP_URL` | - | URL of the LDAP server, e.g., "ldaps://ldap.example.com:1636" for TLS or "ldap://ldap.example.com:389" for non-TLS |
| `LDAP_USER_SEARCH_UNIT` | - | Organizational unit attribute for LDAP user searches, e.g., "ou" |
| `LDAP_USERNAME_ATTRIBUTE` | `uid` | LDAP attribute for username, e.g., "uid" for OpenLDAP or "sAMAccountName" for Active Directory |
| `LDAP_USERNAME_FULL_EMAIL` | `false` | Use full email as username in LDAP authentication (required for user_principal_name auth method) Values: `true`, `false` |

### Api LLM

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_LLM_CONTEXT_LENGTH` | `16000` | Maximum context length for LLM input in tokens, e.g., "16000" or "32000" |
| `BASE64AI_LLM_EMBEDDING_DIMENSIONS` | `2560` | Dimensions for embedding vectors, e.g., "2560" or "1536" |
| `BASE64AI_LLM_INPUT_MAX_TOKENS_EMBEDDINGS` | `6000` | Maximum input tokens for embeddings, e.g., "6000" |
| `BASE64AI_LLM_OUTPUT_MAX_TOKENS` | `2000` | Maximum output tokens for LLM responses, e.g., "2000" or "4096" |
| `BASE64AI_LLM_PLATFORM` | `gpu` | Platform type for LLM inference (GPU or CPU) Values: `gpu`, `cpu` |
| `BASE64AI_LLM_TIMEOUT_MS` | `60000` | Timeout for LLM requests in milliseconds, e.g., "60000" (1 minute) or "120000" (2 minutes) |
| `BASE64AI_MCP_SERVER` | - | URL of the MCP (Model Context Protocol) server, e.g., "http://mcp:8080" |
| `BASE64AI_MERLIN_SERVER` | - | URL of the Merlin LLM server, e.g., "http://merlin:8000" |
| `EMBEDDING_SERVER_ENABLED` | `false` | Enable embedding server for vector search features Values: `true`, `false` |
| `LLM_MODEL` | `local` | LLM model provider to use for AI features Values: `local`, `mock` |

### Api Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `ERROR_STORAGE_PATH` | - | File path for storing error logs, e.g., "/var/log/base64ai/errors" |
| `LOGGING_FORMAT` | `text` | Log output format Values: `json`, `text` |
| `LOGGING_LEVEL` | `http` | Logging level for the application Values: `debug`, `http`, `info`, `warn`, `error` |
| `LOGGING_OUTPUT_PATH` | - | File path for log output, e.g., "/var/log/base64ai/app.log" |

### Api ML Services

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_ABBOT_SERVER` | - | URL of the Abbot server, e.g., "http://abbot:3000" |
| `BASE64AI_CROW_SERVER` | - | URL of the Crow ML server, e.g., "http://crow:5050" |
| `BASE64AI_HAWK_2_SERVER` | - | URL of the Hawk 2 server, e.g., "http://hawk2:5000" |
| `BASE64AI_HAWK_SERVER` | - | URL of the Hawk server, e.g., "http://hawk:5000" |
| `BASE64AI_HERON_SERVER` | - | URL of the Heron server, e.g., "http://heron:3000" |
| `BASE64AI_KIWI_SERVER` | - | URL of the Kiwi server, e.g., "http://kiwi:3000" |
| `BASE64AI_LARK_SERVER` | - | URL of the Lark server, e.g., "http://lark:5050" |
| `BASE64AI_PARROT_SERVER` | - | URL of the Parrot server, e.g., "http://parrot:5050" |
| `BASE64AI_PELICAN_SERVER` | - | URL of the Pelican server, e.g., "http://pelican:3000" |
| `BASE64AI_SEAGULL_SERVER` | - | URL of the Seagull server, e.g., "http://seagull:3000" |
| `BASE64AI_SPARROW_SERVER` | - | URL of the Sparrow server, e.g., "http://sparrow:3000" |
| `BASE64AI_TASK_QUEUE_SERVER` | - | URL of the task queue server (Pheasant) for async processing, e.g., "http://pheasant:3000" |
| `BASE64AI_TOMCAT_SERVER` | - | URL of the Tomcat server, e.g., "http://tomcat:3000" |
| `BASE64AI_TOUCAN_SERVER` | - | URL of the Toucan server, e.g., "http://toucan:3000" |
| `BASE64AI_VULTURE_SERVER` | - | URL of the Vulture server, e.g., "http://vulture:5000" |

### Api Processing

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_DEFAULT_CULTURE` | `en-US` | Default culture/locale for document processing, e.g., "en-US", "de-DE", "fr-FR" |
| `BASE64AI_MAX_PDF_LENGTH` | - | Maximum PDF page count for processing, e.g., "100" or "500" |
| `MAX_IMAGE_SIZE` | `5000` | Maximum image dimension in pixels, e.g., "5000" or "10000" |

### Api Security

| Variable | Default | Description |
|----------|---------|-------------|
| `ALLOW_UNAUTHENTICATED_API_REQUEST` | - | Allow unauthenticated API requests (for On-premises only, not for production) |
| `BASE64AI_RATE_LIMIT_MAX_REQUEST` | `1000` | Maximum number of requests allowed per rate limit window, e.g., "1000" or "5000" |
| `BASE64AI_RATE_LIMIT_WINDOW_MS` | `900000` | Rate limit window in milliseconds, e.g., "900000" (15 minutes) or "3600000" (1 hour) |
| `ENCRYPTION_KEY` | - | Encryption key for sensitive data (32-byte hex string), e.g., "0123456789abcdef0123456789abcdef" |
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "550e8400-e29b-41d4-a716-000005440000" |
| `TASK_QUEUE_SECRET` | - | Secret for task queue authentication, e.g., "task_queue_secret_key" |

### Api Server

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_API_REQUEST_SIZE_LIMIT` | `100mb` | Maximum request body size limit for API requests, e.g., "100mb", "50mb", "200mb" |
| `BASE64AI_HOST_NAME` | - | The hostname for the Base64.ai server that browsers will use to reach the application, e.g., "ultimate.base64.ai" or "docai.example.com" |
| `BASE64AI_HOST_NAME_INTERNAL` | - | Internal hostname for service-to-service communication, e.g., "api-internal", "localhost", or Kubernetes service name like "base64ai-api" |
| `BASE64AI_PROTOCOL` | `http` | Protocol for the Base64.ai server (use "https" for production) Values: `http`, `https` |
| `BASE64AI_PROTOCOL_INTERNAL` | `http` | Protocol for internal Base64.ai server communication Values: `http`, `https` |
| `HTTP_PROXY` | - | HTTP proxy URL for outgoing requests, e.g., "http://proxy.example.com:8080" |
| `HTTPS_PROXY` | - | HTTPS proxy URL for outgoing requests, e.g., "http://proxy.example.com:8080" |
| `PORT` | `3001` | The port number on which the API server listens, e.g., "3001" or "8080" |

### Api Session

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_COOKIE_DESCRIPTOR` | `session.id` | Name of the session cookie, e.g., "session.id" or "base64.session" |
| `BASE64AI_COOKIE_DOMAIN` | - | Domain for session cookies, e.g., ".base64.ai" or ".example.com" |
| `BASE64AI_COOKIE_HTTPONLY` | `false` | Enable HttpOnly flag for session cookies (recommended for security) Values: `true`, `false` |
| `BASE64AI_COOKIE_SECURE` | `false` | Enable Secure flag for session cookies (set to "true" for HTTPS) Values: `true`, `false` |
| `BASE64AI_TTL_SESSION` | `604800000` | Session time-to-live in milliseconds, e.g., "604800000" (7 days) or "86400000" (1 day) |
| `SESSIONSECRET` | - | Secret key for session encryption (use a strong random string), e.g., "my-super-secret-session-key-123" |

### Api Storage

| Variable | Default | Description |
|----------|---------|-------------|
| `FILE_STORAGE_PATH` | - | Local file system path for document storage (on-premises), e.g., "/data/base64ai/files" or "C:\Base64AI\Storage" |

## Sparrow Service

Document AI

### Sparrow Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Sparrow Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Sparrow Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Toucan Service

Document AI

### Toucan Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Toucan Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Toucan Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Tomcat Service

Document AI

### Tomcat Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Tomcat Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Tomcat Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Seagull Service

Document AI

### Seagull Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Seagull Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Seagull Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Pelican Service

Document AI

### Pelican Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Pelican Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Pelican Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Kiwi Service

Document AI

### Kiwi Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Kiwi Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Kiwi Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Heron Service

Document AI

### Heron Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Heron Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Heron Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Abbot Service

Document AI

### Abbot Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Abbot Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Abbot Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Merlin Service

GenAI

### Merlin LLM

| Variable | Default | Description |
|----------|---------|-------------|
| `CTX_WINDOW` | `65536` | Context window size for LLM (max tokens), e.g., "65536", "32768" |
| `EMBEDDING_CTX_WINDOW` | `32768` | Context window size for embedding model, e.g., "32768" |
| `GPU_EMBEDDING_MODEL_NAME` | `flux-M` | Model name for GPU embedding model, e.g., "flux-M" |
| `GPU_MODEL_NAME` | `nexus-L` | Model name for GPU inference, e.g., "nexus-L" |
| `USE_EMBEDDINGS` | `0` | Enable embeddings server alongside chat server Values: `0`, `1` |

### Merlin Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_LEVEL` | `INFO` | Logging level for the ML service Values: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL` |
| `LOGGING_OUTPUT_PATH` | - | Directory path for log output. If not set, logs to stdout. Log file will be named "app.log", e.g., "/var/log" results in "/var/log/app.log" |
| `SERVICE_NAME` | `ml` | Service name identifier for logging and metrics, e.g., "sparrow", "toucan" |

### Merlin Processing

| Variable | Default | Description |
|----------|---------|-------------|
| `CHAT_MEM_RATIO` | `0.8` | Ratio of GPU memory allocated to chat vs embeddings (0.0-1.0), e.g., "0.8" allocates 80% to chat |
| `GPU_MEM` | `0.95` | GPU memory utilization fraction (0.0-1.0), e.g., "0.95" uses 95% of GPU memory |
| `LLM_REQ_HARD_TIMEOUT_SECONDS` | `60` | Hard timeout for LLM requests in seconds, e.g., "60", "120" |
| `NUM_GPU` | `1` | Number of GPUs for tensor-parallel inference, e.g., "1", "2", "4" |
| `SWAP_SPACE` | `4` | GPU swap space in GB, e.g., "4" |

### Merlin Security

| Variable | Default | Description |
|----------|---------|-------------|
| `REQUESTS_CA_BUNDLE_OVERRIDE` | - | Override CA bundle path for HTTP requests, e.g., "/etc/ssl/certs/ca-certificates.crt" |
| `SUBSCRIPTION_KEY` | - | Subscription key for ML cluster authentication (UUID format), e.g., "8b07dafc-1472-4432-9638-ec3bc39594a5" |

### Merlin Server

| Variable | Default | Description |
|----------|---------|-------------|
| `API_HOST` | `http://localhost:3001` | URL of the API server for callbacks and health checks, e.g., "http://api:3001" or "http://ultimate.base64.ai" |
| `INIT_CONTAINER` | - | Run as init container (downloads models only, then exits) Values: `true`, `false` |
| `PORT` | `3000` | Port for the ML service, e.g., "3000" |

## Pheasant Service

Task queue service

### Pheasant Server

| Variable | Default | Description |
|----------|---------|-------------|
| `REDIS_URL` | - | Redis connection URL for task queue, e.g., "redis://redis:6379" |

## Hawk Service

Document AI

### Hawk Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_FORMAT` | `json` | Log output format Values: `json`, `text` |
| `LOGGING_LEVEL` | `Information` | Logging level for the microservice Values: `Information`, `Debug`, `Warning`, `Error` |
| `LOGGING_OUTPUT_PATH` | `/var/log` | File path for log output, e.g., "/var/log" |

### Hawk Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for service authentication |

## Vulture Service

Document AI

### Vulture Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_FORMAT` | `json` | Log output format Values: `json`, `text` |
| `LOGGING_LEVEL` | `Information` | Logging level for the microservice Values: `Information`, `Debug`, `Warning`, `Error` |
| `LOGGING_OUTPUT_PATH` | `/var/log` | File path for log output, e.g., "/var/log" |

### Vulture Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for service authentication |

## Lark Service

Document AI

### Lark Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_FORMAT` | `json` | Log output format Values: `json`, `text` |
| `LOGGING_LEVEL` | `Information` | Logging level for the microservice Values: `Information`, `Debug`, `Warning`, `Error` |
| `LOGGING_OUTPUT_PATH` | `/var/log` | File path for log output, e.g., "/var/log" |

### Lark Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for service authentication |

### Lark Server

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_VULTURE_SERVER` | - | URL of the Vulture server for image processing, e.g., "http://vulture:5000" |

## Parrot Service

Document AI

### Parrot Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_FORMAT` | `json` | Log output format Values: `json`, `text` |
| `LOGGING_LEVEL` | `Information` | Logging level for the microservice Values: `Information`, `Debug`, `Warning`, `Error` |
| `LOGGING_OUTPUT_PATH` | `/var/log` | File path for log output, e.g., "/var/log" |

### Parrot Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for service authentication |

### Parrot Server

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_VULTURE_SERVER` | - | URL of the Vulture server for image processing, e.g., "http://vulture:5000" |

## Crow Service

Document AI

### Crow Logging

| Variable | Default | Description |
|----------|---------|-------------|
| `LOGGING_FORMAT` | `json` | Log output format Values: `json`, `text` |
| `LOGGING_LEVEL` | `Information` | Logging level for the microservice Values: `Information`, `Debug`, `Warning`, `Error` |
| `LOGGING_OUTPUT_PATH` | `/var/log` | File path for log output, e.g., "/var/log" |

### Crow Security

| Variable | Default | Description |
|----------|---------|-------------|
| `SUBSCRIPTION_KEY` | - | Subscription key for service authentication |

### Crow Server

| Variable | Default | Description |
|----------|---------|-------------|
| `BASE64AI_VULTURE_SERVER` | - | URL of the Vulture server for image processing, e.g., "http://vulture:5000" |

