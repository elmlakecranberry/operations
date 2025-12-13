# File Storage: Google Drive

Google Drive is the shared file storage system for Elm Lake Cranberry.

## Role of Google Drive

Google Drive is for:

- Day-to-day document storage
- File sharing and collaboration
- Attachments and supporting documents
- Draft documents and working files
- PDFs, spreadsheets, and reference materials

Drive is a **working space**, not a system of record.

## What Belongs in Google Drive

- SOP drafts before they're finalized in GitHub
- Spreadsheets and working documents
- Scanned documents and PDFs
- Photos and images
- Vendor documents and contracts (copies)
- Meeting notes and temporary collaboration docs
- Report exports from other systems (QuickBooks, OnPay)

## What Does NOT Belong in Google Drive

- **Canonical policies or management decisions** – Those live in the management repo
- **Finalized SOPs and procedures** – Those live in GitHub (operations repo)
- **Sensitive credentials or passwords** – Never store these in Drive
- **Authoritative financial records** – QuickBooks is the source of truth
- **Authoritative employment records** – OnPay is the source of truth

If a document defines authority, policy, or procedure, it should not live only in Drive.

## How Drive Complements GitHub

| Google Drive | GitHub |
|--------------|--------|
| Working documents and drafts | Finalized procedures |
| Attachments and PDFs | Version-controlled text |
| Easy sharing and collaboration | Formal change tracking |
| Casual editing | Structured updates |
| Temporary files | Permanent documentation |

**Workflow example**: Draft an SOP in Google Drive, get feedback, then move the final version to GitHub. Keep supporting attachments (photos, PDFs) in Drive and link to them from the GitHub document.

## Folder Organization

Drive folders should be organized by function, not by date. Suggested structure:

```
Elm Lake Cranberry/
├── Operations/
│   ├── SOP Drafts/
│   ├── Checklists/
│   └── Equipment Manuals/
├── Finance/
│   ├── Reports/
│   └── Invoices/
├── HR/
│   └── Onboarding Materials/
└── Projects/
    └── [Project-specific folders]
```

Avoid creating deeply nested folders. Keep it simple.

## Access and Sharing

- **Internal sharing**: Share folders or files with team members as needed
- **External sharing**: Use "anyone with the link" sparingly and only for non-sensitive materials
- **Permissions**: Default to "Viewer" access; grant "Editor" only when collaboration is needed

## Mobile Access

Google Drive is accessible via:

- Web browser at drive.google.com
- Google Drive mobile app (iOS and Android)
- Desktop app for syncing to local computer

## Getting Help

- **Access issues**: Contact the designated Drive administrator
- **Can't find a file**: Check shared folders or ask the person who created it
- **Storage limits**: Request additional storage through the administrator
