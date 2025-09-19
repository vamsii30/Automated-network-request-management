Automated Network Request Workflow – ServiceNow

This project implements an end-to-end automated workflow in ServiceNow to handle all types of network-related service requests. By leveraging Service Catalog, Flow Designer, custom tables, and approvals, the solution streamlines how requests are submitted, routed, approved, and tracked.

📖 Overview

Organizations frequently receive requests related to network access, device setup, or connectivity issues. Traditionally, these were handled manually, often leading to:

Delays in approvals and assignments.

Miscommunication between employees and IT teams.

Lack of tracking for status and history.

This project addresses those challenges by providing a self-service catalog item with automated workflows that ensures:

Faster request intake.

Automatic approval routing.

Email notifications at each stage.

Centralized visibility for all stakeholders.

🎯 Objectives

Build a user-friendly Service Catalog form for submitting network requests.

Automate backend steps: record creation, approvals, assignments, and updates.

Eliminate unnecessary manual intervention.

Maintain a clear audit trail for compliance and governance.

⚡ Key Features
1. Service Catalog – “Network Request”

A dedicated catalog item designed for network-related services.

Variable sets to capture structured inputs:

Requester Info → Name, Department, Email.

Network Details → Device Type, Location, Justification, Priority.

2. Smart Form Behavior (UI Policies)

Conditional visibility of fields (e.g., extra notes field appears only if Device Type = Others).

Dynamic mandatory rules based on user inputs.

3. Custom Data Table

Created u_network_database_table to act as the system of record.

Fields include: Request Number, Status, Assignment Group, Customer Address, Device Info, Enquiry Date, Assigned To, Updates Count, and Customer Document.

4. Approvals Integration

Linked requests with ServiceNow’s sysapproval_approver framework.

Added a related list to show all approval records directly on the request form.

5. End-to-End Flow Automation

Built in Flow Designer to handle the entire lifecycle:

Extract Data → Capture variables from the catalog form.

Create Record → Save request into the custom table.

Notifications → Auto-send emails to requester and approver.

Approval Task → Request routed for approve/reject decision.

Dynamic Status Update → Status field updates automatically based on flow outcome.

✅ Benefits

Standardized submission of network requests.

Faster processing with automated approvals and notifications.

Single source of truth for all network-related service requests.

Real-time tracking of request progress for employees and managers.
