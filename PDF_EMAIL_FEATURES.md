# PDF and Email Functionality - Implementation Guide

## Overview
The Accident Report Form now includes fully functional PDF generation and email capabilities.

## Features Implemented

### 1. PDF Generation
- **Library Used**: html2pdf.js (v0.10.1) - Industry-standard PDF generation library
- **Button**: "📄 Download PDF" button in the navigation area
- **Functionality**:
  - Generates a complete PDF with all form sections (all 14 tabs)
  - Removes interactive elements (buttons, navigation) from the PDF
  - Creates professional A4 format document
  - Auto-names file: `Accident_Report_[ReportNumber]_[Date].pdf`
  - Shows loading indicator during generation
  - High-quality output (JPEG quality: 98%, scale: 2x)

### 2. Email Functionality
- **Button**: "📧 Email Form" button in the navigation area
- **Functionality**:
  - Opens default email client with pre-filled content
  - Recipient: jeremy@commonsensesafety.co.uk (HSQE Consultant)
  - Subject line includes report number and date
  - Email body includes:
    - Report number
    - Date completed
    - Completer name
    - Instructions for attaching the PDF
  - Offers to generate PDF automatically after opening email client

### 3. Print Functionality (Legacy)
- Browser's native print function still available
- Print-specific CSS hides navigation and shows all sections

## How to Use

### Generate PDF:
1. Fill out the accident report form
2. Click "📄 Download PDF" button
3. Wait for "⏳ Generating PDF..." message
4. PDF will automatically download to your browser's download folder
5. Filename format: `Accident_Report_[Number]_[Date].pdf`

### Email Form:
1. Click "📧 Email Form" button
2. Confirm the instruction dialog
3. Your default email client will open with pre-filled information
4. Generate the PDF when prompted (or do it separately)
5. Attach the PDF to the email
6. Review and send

## Technical Details

### PDF Generation Features:
- **Full document capture**: All 14 tabs included in single PDF
- **Clean output**: Navigation, buttons, and info panels removed
- **Professional formatting**: 10mm margins on all sides
- **High quality**: 2x scale rendering for sharp text
- **Page breaks**: Intelligent page breaking to avoid splitting sections
- **Compression**: PDF compression enabled for smaller file size

### Browser Compatibility:
- Works in all modern browsers (Chrome, Firefox, Safari, Edge)
- Requires JavaScript enabled
- No server-side processing needed (100% client-side)

### Email Compatibility:
- Uses standard `mailto:` protocol
- Works with any email client
- Pre-fills subject and body
- Includes detailed instructions in email body

## Testing

### Test PDF Generation:
1. Open the form in a web browser
2. Fill in at least the Report Number and Date fields
3. Click "📄 Download PDF"
4. Verify PDF downloads with correct filename
5. Open PDF and verify all sections are included

### Test Email:
1. Click "📧 Email Form"
2. Verify email client opens
3. Check recipient, subject, and body are pre-filled
4. Generate PDF when prompted
5. Attach and send test email

## Security & Privacy
- All processing is client-side (no data sent to external servers for PDF generation)
- Form data saved to browser's localStorage only
- PDF generated entirely in the user's browser
- Email uses standard mailto protocol (no data intercepted)

## Troubleshooting

### PDF not generating:
- Check browser console for errors
- Ensure html2pdf.js CDN is accessible
- Try using browser's print function as fallback

### Email not opening:
- Ensure default email client is configured
- Check browser's popup blocker settings
- Manually copy email details if needed

## Files Modified
- `Accident_Report_Form_CSS-HSA-001.html`:
  - Added html2pdf.js CDN link (line 7)
  - Added generatePDF() function (lines 3066-3134)
  - Added emailForm() function (lines 3136-3191)
  - Updated navigation buttons (lines 2858-2859)
  - Added print/PDF CSS styles (lines 600-640)

## Version
- Implementation Date: 2025-11-22
- html2pdf.js Version: 0.10.1
- Form Version: CSS-HSA-001 v2.0
