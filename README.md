# CSS-HSA-001 Accident Report Form & KPI Dashboard

## Overview
This repository contains the CSS-HSA-001 Accident Report Form and integrated KPI Dashboard for Common Sense Safety.

## Components

### 1. Accident Report Form (CSS-HSA-001)
**File**: `Accident_Report_Form_CSS-HSA-001.html`

A comprehensive digital accident/incident report form that includes:
- 15 detailed tabs covering all aspects of accident reporting
- Person affected/injured details
- Incident details and description
- Witness statements
- Minor accident fast-track option
- RIDDOR compliance checking
- Root cause analysis
- Body injury diagrams
- PDF generation and email functionality
- Auto-save to browser localStorage
- **NEW**: Automatic data submission to KPI database

### 2. KPI Dashboard (CSS-HSA-001-KPI)
**File**: `CSS-HSA-001-KPI.html`

An analytics dashboard that provides:
- Real-time accident data analysis
- RIDDOR compliance tracking
- Lost Time Injury Frequency Rate (LTIFR) calculation
- Total Recordable Incident Rate (TRIR) calculation
- Investigation status tracking
- Root cause analysis summaries
- Industry benchmarking
- Data export functionality

## NEW: KPI Integration
The accident report form is now fully integrated with the KPI dashboard. When you save an accident report, the data is automatically:
- Stored in a centralized KPI database
- Used to calculate real-time statistics
- Available for analysis in the KPI dashboard

See **[KPI_INTEGRATION.md](KPI_INTEGRATION.md)** for complete documentation on the integration.

## Quick Start

### Reporting an Accident
1. Open `Accident_Report_Form_CSS-HSA-001.html` in your browser
2. Complete the form tabs with incident details
3. Click "💾 Save & Exit" to save (data is auto-saved to KPI database)
4. Click "📄 Download PDF" to generate a PDF report
5. Click "📧 Email Form" to send via email

### Viewing KPI Dashboard
1. Open `CSS-HSA-001-KPI.html` in your browser, OR
2. Click "📊 View KPI Dashboard" from the accident report form
3. View real-time statistics calculated from all saved accident reports
4. Export data using "📊 Export Data" button
5. Print reports using "🖨️ Print KPI Report" button

## Features

### Accident Report Form Features
- ✅ Multi-tab navigation with progress tracking
- ✅ Auto-save functionality
- ✅ PDF generation
- ✅ Email integration
- ✅ Interactive body diagrams for injury location
- ✅ RIDDOR compliance checking
- ✅ Root cause analysis tools
- ✅ Photo upload capability
- ✅ Witness management
- ✅ Corrective action tracking
- ✅ **NEW**: Automatic KPI data collection

### KPI Dashboard Features
- ✅ Real-time data aggregation
- ✅ RIDDOR statistics
- ✅ Injury metrics (LTIFR, TRIR)
- ✅ Investigation tracking
- ✅ Trend analysis
- ✅ Industry benchmarking
- ✅ Data export (JSON)
- ✅ Print-friendly reports

## Files in This Repository

| File | Description |
|------|-------------|
| `Accident_Report_Form_CSS-HSA-001.html` | Main accident report form |
| `CSS-HSA-001-KPI.html` | KPI Dashboard |
| `KPI_INTEGRATION.md` | Detailed integration documentation |
| `PDF_EMAIL_FEATURES.md` | PDF and email functionality documentation |
| `README.md` | This file |

## Technical Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- localStorage support (for data persistence)
- Internet connection (for external CSS libraries)

## Data Storage

Data is stored locally in the browser's localStorage:
- `accidentReportForm` - Current form draft data
- `accidentKPIDatabase` - Aggregated accident records for KPI analysis

**Note**: Data is browser-specific and persists across sessions. Clearing browser data will erase stored information.

## Compliance

This system complies with:
- HSE RIDDOR reporting requirements
- GDPR data protection legislation
- UK health and safety regulations
- HSG65 guidance documents

## Support & Contact

**HSQE Consultant**: Jeremy Bromley
**Email**: jeremy@commonsensesafety.co.uk
**Organization**: Common Sense Safety

## Version History

### Version 2.0 (November 2025)
- ✅ Added KPI Dashboard integration
- ✅ Automatic data collection and aggregation
- ✅ Real-time statistics calculation
- ✅ Data export functionality
- ✅ Enhanced navigation between forms

### Version 1.0 (January 2025)
- Initial release with PDF and email functionality

## License

© 2025 Common Sense Safety
CONFIDENTIAL - For Official Use Only
