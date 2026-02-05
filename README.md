AI-Powered LinkedIn Content Engine (n8n)
Overview:
The AI-Powered LinkedIn Content Engine is an end-to-end automation built with n8n that transforms structured inputs into high-quality, publish-ready LinkedIn posts using large language models and event-driven workflows.
The system continuously monitors a Google Sheet for new or updated content, summarizes source material using Google Gemini, refines it into a professional LinkedIn post format, and publishes it automatically via the LinkedIn API. The workflow is designed to be modular, extensible, and production-ready, demonstrating how modern AI models can be integrated into reliable business automations rather than used in isolation.


All external integrations in this project are authenticated using OAuth 2.0 or n8n-managed credentials. No API keys, OAuth tokens, or secrets are stored in the workflow export or committed to this repository.



What This Project Solves
Creating consistent, high-quality LinkedIn content is time-consuming and difficult to scale. Most AI demos stop at prompt engineering, but real systems must handle:
Event-driven triggers
Multi-step content transformations
Secure credential management
Platform-specific formatting
Reliable publishing via APIs
This project showcases real-world skills in:
Workflow orchestration with n8n
LLM integration using Google Gemini
API-driven automation (Google Sheets, LinkedIn)
Secure credential management and deployment-ready design, 
Clean separation of logic, prompts, and integrations
This project provides a repeatable, secure content pipeline that converts structured ideas or articles into polished LinkedIn posts with minimal manual effort.
High-Level Workflow
Trigger A change in a Google Sheet row (new content or update) triggers the workflow.
Summarization Source text or article links are summarized using Google Gemini.
Post Generation A second LLM chain rewrites the summary into a LinkedIn-optimized post with appropriate tone and structure.
Publishing The final post is published automatically via the LinkedIn API.

Authentication & OAuth Configuration
This workflow uses OAuth 2.0–based authentication and n8n-managed credentials for all third-party integrations. Authentication is configured locally within the user’s n8n instance and is intentionally excluded from the exported workflow JSON to ensure safe open-source sharing.
OAuth-Based Integrations
Google Sheets (OAuth 2.0): Used to trigger the workflow and read structured content.
LinkedIn API (OAuth 2.0): Used to publish generated posts to LinkedIn.
OAuth authorization flows are handled entirely by n8n. Access tokens are stored securely and refreshed automatically.
API Key–Based Integration
Google Gemini: Uses an API key stored securely via an n8n credential. The key is never embedded in the workflow export.
Why This Project Matters
Unlike single-script AI examples, this project demonstrates:
Production-style automation using a visual workflow engine
Composable AI chains rather than monolithic prompts
Real API integrations with authentication and rate considerations
Safe open-source practices, including sanitized exports and environment isolation
Use Cases
Personal LinkedIn content automation
Team-level content pipelines
Reference architecture for AI-powered workflow orchestration
A personal content engine
