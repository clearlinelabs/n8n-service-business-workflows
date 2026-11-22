# n8n workflows for service businesses

Free, tested n8n workflows for contractors, property managers and agencies, built around Google Sheets + Gmail. Each one was run end-to-end inside n8n (including the empty-sheet case) before publishing.

## Free workflows

| Workflow | What it does | Starter |
|---|---|---|
| [Missed Call Text-Back](workflows/missed-call-textback.json) | When you miss a call, the caller gets a text within seconds ('Sorry we missed you — how can we help?') and the lead is logged. | [starter sheet](https://docs.google.com/spreadsheets/d/1ZRAdDCmg9spx1caXlyuVfWjnLT6Tyyu0fGe-0qlmE64/copy) |
| [Google Review Request Autopilot](workflows/review-requests.json) | Every finished job gets a polite review request (email + optional SMS) and one reminder — more 5-star reviews on autopilot. | [starter sheet](https://docs.google.com/spreadsheets/d/1VCCw8rXYUGX9unftKeQEXmbOJ61EMhDduA4pCvXbHEY/copy) |
| [Overdue Invoice Reminder Sequence](workflows/invoice-reminders.json) | Friendly → firm → final reminders at 3, 10 and 20 days overdue, logged in your sheet. Get paid faster without awkward calls. | [starter sheet](https://docs.google.com/spreadsheets/d/1uQ7lc2KeayZCNimM6FyrFF_uU-Za8vXoW8IF2qWijk8/copy) |
| [Payment Received → Thank-You Receipt](workflows/payment-receipts.json) | When an invoice is marked paid, the customer instantly gets a clean thank-you receipt by email — professional, automatic, logged. | [starter sheet](https://docs.google.com/spreadsheets/d/1p9MW8KeWAGQ6RTYavvfaQ4wuN4gTKFsbM630AcECs5I/copy) |
| [Referral Request Sequence](workflows/referral-asks.json) | Two weeks after a happy job, customers get a friendly referral ask with your offer — word-of-mouth on autopilot. | [starter sheet](https://docs.google.com/spreadsheets/d/1av8K9wh6-7R9pUVXgxdSMkAjv6X0Yaeh472QfzPZGZU/copy) |
| [Vendor Work Order Dispatch & Follow-Up](workflows/vendor-dispatch.json) | Assign a vendor and they get a clean work order by email; no confirmation in 24 h → up to 2 polite follow-ups, then you're alerted. | [starter sheet](https://docs.google.com/spreadsheets/d/1KuvWKOBgLaW4cPLU-k51emicWEKGk-czp2tgpujuc9c/copy) |

### How to use
1. In n8n: **Workflows → Import from file** → pick the `.json`.
2. Make a copy of the starter Google Sheet (link above) and paste its ID into the **Config** node.
3. Connect your Google Sheets / Gmail (and Twilio where used) credentials, test with your own email, then activate.

Keep tab names and column headers as in the starter sheet - the workflows read them.

## More workflows
The full library has 30 workflows (AI booking intake, vendor dispatch with follow-ups, tenant FAQ auto-answers, self-improving content calendar, AI lead scoring and more):

- Website Lead → Instant AI Reply + CRM
- Estimate Follow-Up Sequence
- AI Inbox Triage & Draft Replies
- Weekly Owner KPI Email
- Lease Renewal Reminders (90/60/30)
- Monthly Owner Statement Emailer
- New Client Onboarding Sequence
- Appointment Reminder Autopilot
- Maintenance Plan Renewals & Tune-Up Reminders
- Won Quote → Invoice
- Customer Feedback & Rescue
- Tenant Maintenance Request Intake (AI triage)
- Vendor Bill Capture (AI)
- Monthly Client Hours Report (Agencies)
- Daily Crew Schedule Email
- AI Booking Intake (No Phone Tag)
- On-My-Way & Running-Late Alerts
- Job Photo to Social Post (AI, with approval)
- 5-Star Review to Testimonial Post
- Self-Improving Weekly Content Calendar (AI)
- Vendor Work Order Dispatch & Follow-Up
- Tenant Maintenance Status Updates
- Tenant FAQ Auto-Answer Drafts (AI)
- Customer Feedback Collector & Insight Log (AI)
- AI Lead Qualifier & Hot-Lead Alert

Full library, setup guides and done-for-you installation: **https://payhip.com/ClearlineSheets90**

- Don't want to set it up yourself? **Template Setup, $249**: https://payhip.com/b/TDyEN
- Not sure what to automate first? **Automation Audit, $297** (credited toward setup): https://payhip.com/b/TdWmA
- Agencies: **White-label license for all 30 workflows**: https://payhip.com/b/Ac9Vp

## Feedback
Found a bug or want a workflow for your trade? Open an issue - every report improves the next version.

License: MIT · Maintained by Clearline Labs
