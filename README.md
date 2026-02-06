# File Name Generator

A simple, interactive web-based tool for generating standardized file names following a specific naming convention.

## Features

- **Project Name** – Required field for the project identifier
- **Part Number** – Optional field for part/SKU identification
- **Short Description** – Required field with 25-character limit and live character counter
- **Create Date** – Date picker that formats the date as MMDDYY
- **Revision** – Increment/decrement buttons to manage revision numbers (Rev01, Rev02, etc.)
- **Owner Initial** – Optional field for owner identification (max 3 characters)
- **Live Preview** – Real-time filename generation as you enter data
- **Copy Button** – One-click copy to clipboard with confirmation toast
- **Reset Button** – Clear all fields and start fresh

## Filename Pattern

```
<Project>-<PartNo>-<Desc>-<MMDDYY>-<Rev>-<Owner>
```

*Optional fields (Part Number and Owner Initial) are automatically excluded if left empty.*

### Space Handling

All spaces in input fields are automatically replaced with underscores (`_`) in the generated filename.

### Example Output

Input:
- Project Name: `ACME Widget`
- Part Number: `P123`
- Description: `Assembly Guide`
- Create Date: `02/06/2026`
- Revision: `Rev02`
- Owner Initial: `JD`

Output:
```
ACME_Widget-P123-Assembly_Guide-020626-Rev02-JD
```

## Usage

1. Open `filename-generator.html` in any modern web browser
2. Fill in the required fields (Project Name, Description, Date, Revision)
3. Optionally add Part Number and Owner Initial
4. Use the **−** and **+** buttons to adjust the revision number
5. Watch the filename preview update in real-time
6. Click the **Copy** button to copy the filename to your clipboard
7. Use the **Reset** button to clear all fields

## Revision Control

- Click **+** to increment the revision (Rev01 → Rev02 → Rev03, etc.)
- Click **−** to decrement the revision (stops at Rev01)
- Revision number always displays with zero-padding (Rev01, Rev02, etc.)

## Browser Compatibility

Works with all modern browsers that support:
- ES6 JavaScript
- HTML5 Date input
- Clipboard API

## Files

- `filename-generator.html` – Complete standalone HTML file with embedded CSS and JavaScript
