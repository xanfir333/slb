[README.md](https://github.com/user-attachments/files/32746951/README.md)
# Import Guarantee Tracker

A browser-based tool for processing and cross-checking Customs Declaration PDFs and Commercial Invoice Excel files.

## Overview

Import Guarantee Tracker is a client-side web application designed to help organize import documentation into a single tracking table.

The application can:

- Upload a Customs Declaration PDF
- Upload a Commercial Invoice Excel file
- Extract customs declaration information
- Extract invoice information and product lines
- Detect MRN, declaration date, declarant, importer and customs regime
- Detect Transport Number from the invoice or customs declaration
- Extract invoice product line, part number and serial number
- Cross-check invoice HTC/customs codes against customs declaration articles
- Display matched and unmatched invoice lines
- Keep manual tracking fields editable
- Copy the generated table directly into Excel

## Main workflow

1. Upload the Customs Declaration PDF.
2. Upload the Commercial Invoice Excel file.
3. Click **Generate Tracker**.
4. The extracted information is displayed in the tracking table.
5. Review the validation report.
6. Complete the manual fields:
   - Transport Document
   - Guarantee Paid
   - Guarantee Claimed
   - Closed
7. Use **Copy Table** to copy the table into Excel.

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- PDF.js for PDF text extraction
- SheetJS / XLSX for Excel file processing

The current version is a static client-side application. The external libraries are loaded from CDN resources.

## Privacy

Document processing is designed to take place in the user's browser. The current application does not require a backend server.

Do **not** place real Customs Declarations, Commercial Invoices, MRNs, EORI numbers or other confidential documents inside the GitHub repository.

Before using the application with confidential company documents in a public environment, verify your organization's security and data-protection requirements.

## GitHub Pages

This project can be hosted as a static website using GitHub Pages.

Recommended repository structure:

```text
import-guarantee-tracker/
├── index.html
├── README.md
└── .gitignore
```

The application file should be named `index.html`.

For a project repository, the website will normally be available at:

```text
https://YOUR-USERNAME.github.io/import-guarantee-tracker/
```

## How to publish

1. Create a new GitHub repository.
2. Name it something like `import-guarantee-tracker`.
3. Upload the application as `index.html`.
4. Upload this `README.md`.
5. Open **Settings → Pages**.
6. Under **Build and deployment**, select **Deploy from a branch**.
7. Select the `main` branch.
8. Select the `/ (root)` folder.
9. Click **Save**.
10. Wait for GitHub Pages to deploy the website.

GitHub will then provide the live website address.

## Important: public website vs private documents

The website can be public while the documents remain on the user's computer.

Users do not need to upload their PDFs or Excel files to GitHub. They select the files locally through the browser, and the JavaScript processes them.

Do not store real company documents in the repository.

## Current limitations

The application is based on document structures and extraction rules. Different suppliers, customs systems or invoice templates may use different labels and layouts.

Therefore:

- Some Transport Numbers may require additional extraction rules.
- Some Serial Numbers may not be present in the source document.
- PDF text extraction depends on how the PDF was generated.
- Scanned/image-only PDFs may require OCR in a future version.
- Different Excel invoice templates may require additional mapping rules.
- HTC/customs-code matching uses normalization and compatibility rules and should be reviewed for critical customs decisions.

## Future development

Possible improvements include:

- OCR for scanned Customs Declarations
- Drag-and-drop document upload
- Multiple PDF and Excel uploads
- Automatic document grouping
- Duplicate detection
- Better invoice template recognition
- More robust Transport Number detection
- Automatic Serial Number extraction
- Visual match indicators
- Direct `.xlsx` export
- Save/load tracker sessions
- User authentication
- Company-specific configurations
- Database storage
- Audit history
- Custom domain
- Responsive mobile/tablet interface

## License

Choose an appropriate license before publishing the project publicly.

If the application contains proprietary company logic or business processes, consider keeping the repository private or selecting a license that matches your intended distribution model.

## Disclaimer

This application is a document-processing and tracking aid. Extracted information should be reviewed against the original Customs Declaration and Commercial Invoice before being used for customs, financial, compliance or other business-critical decisions.
