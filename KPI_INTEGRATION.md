# CSS-HSA-001 KPI Integration Documentation

## Overview
The CSS-HSA-001 Accident Report Form is now integrated with the CSS-HSA-001-KPI Dashboard to provide real-time analytics and key performance indicators (KPIs) for accident data management.

## Features

### 1. Automated Data Collection
- When an accident report form (CSS-HSA-001) is saved, the data is automatically stored in a centralized KPI database
- Data is stored in the browser's localStorage for persistent storage
- Each accident report creates or updates a record in the KPI database

### 2. KPI Dashboard
- **Real-time Statistics**: The dashboard automatically calculates and displays statistics from all saved accident reports
- **RIDDOR Compliance Tracking**: Monitors and reports on RIDDOR reportable incidents
- **Injury Metrics**: Calculates LTIFR (Lost Time Injury Frequency Rate) and TRIR (Total Recordable Incident Rate)
- **Investigation Status**: Tracks the progress of accident investigations

### 3. Key Metrics Calculated

#### RIDDOR Compliance
- Fatal incidents count
- Specified injuries count
- Over-7-day injuries count
- Dangerous occurrences count
- Occupational diseases count
- HSE reporting compliance percentage

#### Incident Statistics
- Total incidents
- RIDDOR reportable incidents
- Non-RIDDOR incidents
- Near misses reported
- Environmental incidents
- Property damage incidents

#### Injury Metrics
- Lost Time Injuries (LTI)
- Total days lost to injury
- Lost Time Injury Frequency Rate (LTIFR)
  - Formula: (LTI × 100,000) ÷ Total hours worked
- Average Severity Rate
- Total Recordable Incident Rate (TRIR)
  - Formula: (Total recordable incidents × 200,000) ÷ Total hours worked
- Medical treatment cases

#### Investigation Tracking
- Awaiting investigation count
- In progress investigations count
- Completed investigations count
- Outstanding actions count

## How It Works

### Data Flow
1. User fills out CSS-HSA-001 Accident Report Form
2. User clicks "Save & Exit" button
3. Form data is saved to localStorage for form persistence
4. Form data is simultaneously saved to the KPI database in a structured format
5. KPI Dashboard reads from the KPI database and calculates statistics
6. Dashboard displays real-time analytics based on all saved reports

### Data Storage
Data is stored in the browser's localStorage under the key `accidentKPIDatabase` as a JSON array of accident records.

Each record contains:
- Report identification (ID, report number, timestamp)
- Person details (name, age, gender)
- Incident classification (type, RIDDOR status)
- Injury details (type, body part, severity)
- Time loss information (days lost, LTI status)
- Investigation status and completion
- Root cause analysis data
- Location and department information
- Corrective actions
- Metadata (completed by, date)

### Navigation Between Forms
- **From Accident Report to KPI Dashboard**: Click the "📊 View KPI Dashboard" button
- **From KPI Dashboard to Accident Report**: Click the "← Return to Accident Report Form" button

## Using the System

### Creating Accident Reports
1. Open `Accident_Report_Form_CSS-HSA-001.html`
2. Fill in the accident details across all tabs
3. Click "💾 Save & Exit" to save the form
4. Data is automatically added to the KPI database

### Viewing KPI Dashboard
1. From the accident report form, click "📊 View KPI Dashboard"
2. Alternatively, open `CSS-HSA-001-KPI.html` directly
3. The dashboard will automatically load and display statistics from all saved reports

### Exporting Data
1. Open the KPI Dashboard
2. Click "📊 Export Data" button
3. A JSON file containing all accident records will be downloaded
4. File format: `accident_kpi_data_YYYY-MM-DD.json`

### Printing Reports
1. Open the KPI Dashboard
2. Click "🖨️ Print KPI Report" button
3. Use your browser's print dialog to print or save as PDF

## Technical Details

### Browser Compatibility
- Requires a modern browser with localStorage support
- Tested on Chrome, Firefox, Safari, and Edge

### Data Persistence
- Data is stored in browser localStorage
- Data persists across browser sessions
- Data is browser-specific (not shared between different browsers)
- Clearing browser data will erase the KPI database

### Data Capacity
- localStorage typically supports 5-10MB of data
- Each accident record is approximately 1-2KB
- Can store thousands of accident reports

### Limitations
- Data is stored locally in the browser only
- Data is not synchronized between different computers/browsers
- For multi-user environments, consider server-based storage

## Maintenance

### Clearing Data
For testing or maintenance purposes, you can clear the KPI database:
1. Open browser developer console (F12)
2. Type: `localStorage.removeItem('accidentKPIDatabase')`
3. Press Enter
4. Refresh the page

### Backing Up Data
Export data regularly using the "📊 Export Data" button to create backups of your accident records.

### Updating Hours Worked
The dashboard uses a default value of 140,280 hours worked for calculations. To change this:
1. Edit `CSS-HSA-001-KPI.html`
2. Find the `calculateInjuryMetrics` function
3. Update the `totalHoursWorked` variable
4. Save and reload the dashboard

## Compliance

This integration maintains compliance with:
- HSE RIDDOR reporting requirements
- GDPR data protection legislation
- HSG65 guidance documents
- UK health and safety regulations

## Support

For questions or issues with the KPI integration:
- Contact: Jeremy Bromley
- Email: jeremy@commonsensesafety.co.uk
- Organization: Common Sense Safety

## Version Information
- **Integration Version**: 1.0
- **Release Date**: November 2025
- **Form Version**: CSS-HSA-001 v2.0
- **Dashboard Version**: CSS-HSA-001-KPI v1.0
