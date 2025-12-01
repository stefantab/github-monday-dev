# Configuration — GitHub for monday dev

## Mapping
- Board: Select your monday board (Sprint / Kanban / Bugs).
- Columns:
  - `PR Status` (status): Open, Draft, Ready for Review, Merged, Closed
  - `Review Status` (status): Changes Requested, Approved, Pending
  - `Checks` (status/text): Pass, Fail, Pending
  - `PR Link` (link): PR URL

## Linking options
- Smart linking via branch or PR title keywords (e.g., DEV-123).
- Manual “Link PR” action in the app.

## Webhooks
- Events: pull_request, pull_request_review, check_suite, check_run, push, issue_comment (optional).
- Delivery: Signed with secret; 2‑retry backoff.

## Permissions
- GitHub App scopes: Metadata, Contents:Read, Pull requests:Read, Checks:Read
- monday: per-user OAuth with least‑privilege scopes.

## Rate limits
- Queue processing with exponential backoff; idempotent updates.

## Logging
- Structured JSON logs; PII minimized; retention 30–90 days (configurable).
