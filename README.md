# n8n Workflows Portfolio

Automation workflows I've built in [n8n](https://n8n.io) for small businesses, mainly property management, AI customer service, and finance/back-office work.

**61 workflows, 1129 nodes total.**

My background is 15+ years in compliance auditing, so I build with audit trails, error handling, and clear business rules in mind. The 10-part maintenance system is the best example of that.

## How to use these files

Each `.json` file is an n8n workflow export. To view or reuse one: in n8n, create a new workflow, open the menu (…), choose **Import from File**, and select the file. You'll need to connect your own credentials.

## Data cleaning

These are copies of working workflows with private details removed: client names are replaced with generic labels, test data and internal IDs are stripped, webhook paths and sheet IDs are replaced with placeholders, and saved credentials are not included (only their type).

## Property management: 10-part maintenance system

A connected set of workflows that runs a maintenance request from intake to close: tenant acknowledgment, urgency classification, SLA monitoring, vendor assignment, status updates, completion confirmation, an audit log, error handling, missed-call follow-up, and a manual urgency override.

| Workflow | Nodes | Main tools |
|---|---|---|
| [01 - AppFolio Work Order Received → Tenant Acknowledgment](property-management/maintenance-system/01-appfolio-work-order-received-to-tenant-acknowledgment.json) | 27 | Webhook, dataTable, Twilio, Gmail, HTTP/API |
| [02 - Urgency Classification + Task Routing](property-management/maintenance-system/02-urgency-classification-task-routing.json) | 58 | dataTable, HTTP/API, Gmail |
| [03 - SLA Monitor](property-management/maintenance-system/03-sla-monitor.json) | 10 | Schedule, dataTable |
| [04 - Vendor Assignment](property-management/maintenance-system/04-vendor-assignment.json) | 21 | Gmail, Slack |
| [05 - Tenant Status Updates](property-management/maintenance-system/05-tenant-status-updates.json) | 25 | Webhook, Twilio, Email |
| [06 - Completion Confirmation](property-management/maintenance-system/06-completion-confirmation.json) | 22 | Twilio, Gmail, HTTP/API |
| [07 - Audit Logger](property-management/maintenance-system/07-audit-logger.json) | 22 | HTTP/API, dataTable |
| [08 - Error Handler](property-management/maintenance-system/08-error-handler.json) | 28 | Slack, Google Sheets |
| [09 - Missed Call Follow-Up](property-management/maintenance-system/09-missed-call-follow-up.json) | 21 | Webhook, HTTP/API, Twilio, Gmail, dataTable |
| [10 - Manual Urgency Override](property-management/maintenance-system/10-manual-urgency-override.json) | 18 | Webhook, HTTP/API, Slack, Gmail |

## Property management

Maintenance triage, emergency escalation, AppFolio-based automation, rental lead handling, and an AI assistant for property managers.

| Workflow | Nodes | Main tools |
|---|---|---|
| [AppFolio Maintenance Workflow](property-management/appfolio-maintenance-workflow.json) | 114 | Webhook, AI Agent, Gmail, HTTP/API, Twilio, Schedule |
| [AppFolio Property Management Automation](property-management/appfolio-property-management-automation.json) | 28 | Webhook, Slack, HTTP/API, Twilio, Schedule |
| [Emergency Maintenance Escalation](property-management/emergency-maintenance-escalation.json) | 10 | Webhook, Slack, Twilio, Email |
| [Maintenance Request Auto-Triage (Claude) - Full with Fallbacks](property-management/maintenance-request-auto-triage-claude-full-with-fallbacks.json) | 17 | Google Sheets, Gmail, Slack, Webhook, HTTP/API |
| [Maintenance Request Auto-Triage](property-management/maintenance-request-auto-triage.json) | 31 | Google Sheets, Webhook, HTTP/API, Gmail, Slack, Schedule |
| [Property Management AI Assistant](property-management/property-management-ai-assistant.json) | 82 | AI Agent, Webhook, Slack, Google Sheets, Twilio, Email |
| [RentEngine Lead Automation](property-management/rentengine-lead-automation.json) | 27 | Webhook, dataTable, Twilio, Slack, Schedule |

## AI customer service and phone/SMS

AI receptionists, WhatsApp and SMS auto-responders, missed-call follow-up, opt-out handling, and lead intake and routing.

| Workflow | Nodes | Main tools |
|---|---|---|
| [AI-Powered SMS Auto-Responder with Twilio](ai-customer-service/ai-powered-sms-auto-responder-with-twilio-v2.json) | 8 | AI Agent, Claude, Twilio, Webhook |
| [AI-Powered SMS Auto-Responder with Twilio](ai-customer-service/ai-powered-sms-auto-responder-with-twilio.json) | 8 | AI Agent, Claude, Twilio, Webhook |
| [AI Receptionist for Restaurant (GoHighLevel)](ai-customer-service/ai-receptionist-for-restaurant-gohighlevel.json) | 39 | Webhook, AI Agent, Twilio, HTTP/API, Google Sheets, Gmail |
| [GoHighLevel SMS/Email Automation](ai-customer-service/gohighlevel-sms-email-automation.json) | 44 | Webhook, HTTP/API, dataTable |
| [RingCentral Inbound Calls](ai-customer-service/ringcentral-inbound-calls.json) | 46 | Webhook, HTTP/API, Twilio, Slack, AI Agent, Gmail |
| [RingCentral Missed Call Follow-up](ai-customer-service/ringcentral-missed-call-follow-up.json) | 15 | Webhook, Google Sheets, HTTP/API, Gmail, Slack |
| [RingCentral SMS Opt-Out Handler](ai-customer-service/ringcentral-sms-opt-out-handler.json) | 7 | Webhook, Google Sheets, HTTP/API, Gmail |
| [Roofing Contractor AI Lead Intake & Routing](ai-customer-service/roofing-contractor-ai-lead-intake-routing.json) | 13 | Webhook, HTTP/API, Twilio, Gmail, Google Sheets |
| [SMS Opt-Out Handler](ai-customer-service/sms-opt-out-handler.json) | 8 | Webhook, Google Sheets, HTTP/API, Gmail |
| [WhatsApp AI Customer Service](ai-customer-service/whatsapp-ai-customer-service.json) | 63 | WhatsApp, AI Agent, HTTP/API, dataTable, Telegram, Webhook |

## Finance and documents

Invoice detection, collection, data extraction, and document search.

| Workflow | Nodes | Main tools |
|---|---|---|
| [Automated Invoice Email Detection and Trigger](finance-and-documents/automated-invoice-email-detection-and-trigger.json) | 27 | Email, AI Agent, Claude, dataTable, Slack |
| [Automated Invoice Processing and Data Extraction](finance-and-documents/automated-invoice-processing-and-data-extraction.json) | 18 | Google Drive, HTTP/API, AI extraction, lmChatOpenRouter, Google Sheets |
| [Automated Invoice Processing](finance-and-documents/automated-invoice-processing.json) | 17 | Google Drive, mindee, AI extraction, quickbooks, Claude |
| [Email Invoice Retrieval and Response Generator for Printify Store](finance-and-documents/email-invoice-retrieval-and-response-generator-for-printify-store.json) | 8 | microsoftOutlookTrigger, HTTP/API, AI Agent, Claude |
| [Multi-Source Invoice Collection and Centralization](finance-and-documents/multi-source-invoice-collection-and-centralization.json) | 5 | Gmail, Webhook, postgres, Schedule |
| [P8 – Document Search](finance-and-documents/p8-document-search.json) | 6 | Gemini embeddings, Pinecone |

## Marketing

Ad performance monitoring and scheduled social media posting.

| Workflow | Nodes | Main tools |
|---|---|---|
| [Facebook Auto Post](marketing/facebook-auto-post.json) | 22 | Schedule, Google Drive, HTTP/API, Slack, Gmail, Google Sheets |
| [Google Drive - Meta ads](marketing/google-drive-meta-ads.json) | 14 | Schedule, Google Drive, HTTP/API, Slack, Gmail |
| [Meta Ad Monitoring](marketing/meta-ad-monitoring.json) | 22 | Schedule, HTTP/API, Gmail, Slack |
| [Meta Performance Monitor](marketing/meta-performance-monitor.json) | 13 | Schedule, HTTP/API, Gmail, Slack |

## Experiments and tests

Learning builds, prototypes, and test workflows. Included to show range; less polished than the folders above.

| Workflow | Nodes | Main tools |
|---|---|---|
| [Gmail Integration Setup](experiments-and-tests/gmail-integration-setup.json) | 7 | AI Agent, Gmail, Google Sheets, Gemini |
| [My Sub-Workflow 1](experiments-and-tests/my-sub-workflow-1.json) | 2 | Core logic nodes |
| [My Sub-Workflow 2](experiments-and-tests/my-sub-workflow-2.json) | 2 | Core logic nodes |
| [My workflow 10](experiments-and-tests/my-workflow-10.json) | 35 | Schedule, Google Sheets, Slack |
| [My workflow 11](experiments-and-tests/my-workflow-11.json) | 12 | Schedule, Google Sheets, Slack |
| [My workflow 12](experiments-and-tests/my-workflow-12.json) | 0 | Core logic nodes |
| [My workflow 13](experiments-and-tests/my-workflow-13.json) | 0 | Core logic nodes |
| [My workflow 14](experiments-and-tests/my-workflow-14.json) | 38 | Webhook, HTTP/API, Twilio, Gmail, Google Sheets, Google Calendar |
| [My workflow 15](experiments-and-tests/my-workflow-15.json) | 15 | Webhook, dataTable, Twilio, Slack |
| [My workflow 16](experiments-and-tests/my-workflow-16.json) | 6 | Schedule, dataTable, Twilio, Slack |
| [My workflow 17](experiments-and-tests/my-workflow-17.json) | 6 | Webhook, Twilio, dataTable, Slack |
| [My workflow 18](experiments-and-tests/my-workflow-18.json) | 0 | Core logic nodes |
| [My workflow 2](experiments-and-tests/my-workflow-2.json) | 7 | Core logic nodes |
| [My workflow 20](experiments-and-tests/my-workflow-20.json) | 0 | Core logic nodes |
| [My workflow 21](experiments-and-tests/my-workflow-21.json) | 0 | Core logic nodes |
| [My workflow 3](experiments-and-tests/my-workflow-3.json) | 5 | Core logic nodes |
| [My workflow 4](experiments-and-tests/my-workflow-4.json) | 1 | Core logic nodes |
| [My workflow 5](experiments-and-tests/my-workflow-5.json) | 6 | GitHub, Gemini |
| [My workflow 6](experiments-and-tests/my-workflow-6.json) | 3 | Chat, Gemini |
| [My workflow 7](experiments-and-tests/my-workflow-7.json) | 5 | Chat, AI Agent, Gemini |
| [My workflow 8](experiments-and-tests/my-workflow-8.json) | 7 | Chat, AI Agent, Gemini, githubTool |
| [My workflow 9](experiments-and-tests/my-workflow-9.json) | 6 | GitHub, Pinecone, Gemini embeddings, Document loader |
| [My workflow](experiments-and-tests/my-workflow.json) | 1 | Core logic nodes |
| [QA](experiments-and-tests/qa.json) | 1 | Core logic nodes |

## Contact

Michael Karetko, AutomateMe360: [automateme360.com](https://automateme360.com)
