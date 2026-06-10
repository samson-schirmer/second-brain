---
title: Writer Connectors Access
type: initiative
status: active
created: 2026-06-10
last_reviewed: 2026-06-10
sources:
  - "Attached Context: Team Coordination and Updates_otter.ai.txt"
relates_to:
  - page: "[[writer-agent-deployment]]"
    rel: supports
  - page: "[[platform-integration]]"
    rel: supports
  - page: "[[marketing-workflow-transformation]]"
    rel: supports
---

# Writer Connectors Access

**What:** Access path for Writer connectors into Microsoft services: Outlook, Teams, SharePoint, OneDrive, and Calendar.

**Status:** Active enablement. Users were receiving connector errors until they requested the required access.

**Access path:** Go through My Comcast Access, search for Writer, and request the item called MCP server. Samson can approve access after the request is submitted.

**After approval:** Users still need to manually click Connect in Writer and authenticate. Once authenticated, the connector can be attached to a Writer session or playbook.

**Use cases mentioned:**

- Prioritize inbox and draft email replies in Samson's tone, saved as Outlook drafts.
- Search Teams messages for recent mentions.
- Search SharePoint/OneDrive for files, especially when the user can provide a partial title or folder context.

**Practical constraint:** SharePoint search may take back-and-forth. The more specific the prompt is about title, folder, or context, the faster Writer can find the right file.
