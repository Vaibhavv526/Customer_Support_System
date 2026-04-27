# Core Platform
n8n (workflow automation)

# AI / LLM APIs
OpenAI API / OpenRouter API
- Chat Model (LLM classification)
- Embeddings (if extended in future)

# Email Integration
Gmail API OR IMAP Email Server
- IMAP (imap.gmail.com, port 993)
- SMTP (smtp.gmail.com, port 587)

# Database
PostgreSQL
- Used for storing issue tickets

# Cloud / Storage (Optional)
Google Sheets API
- Used for temporary logging

# Authentication
Google OAuth 2.0 (for Gmail & Sheets)
App Password (for IMAP if Gmail used)

# Environment / Runtime
Docker (optional for deployment)
Node.js (if running n8n locally)

# System Requirements
Port: 5678 (n8n)
PostgreSQL Port: 5432

# Optional Extensions (Future Scope)
Vector Database (Pinecone / Qdrant / Supabase pgvector)
Slack / Discord Webhooks
