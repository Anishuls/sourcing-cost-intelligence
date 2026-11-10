# Sourcing Cost Intelligence

A desktop application for analyzing procurement data and supplier cost comparison.

## Overview

**Sourcing Cost Intelligence** is a local-first desktop tool that analyzes purchase order data to identify cost optimization opportunities. It compares supplier pricing, detects overpayments, and generates detailed procurement analytics reports.

### Key Features

- 🔍 **Supplier Price Comparison** - Compare pricing across multiple suppliers for the same items
- 💰 **Cost Analysis** - Identify overpayments and calculate potential savings
- 📊 **Price Ladder Analysis** - View cheapest, middle, and highest supplier pricing
- 👥 **Cross-Buyer Analysis** - Detect price variance across different buyers
- 📈 **Reporting** - Export detailed analysis to formatted Excel reports
- 🔒 **Privacy First** - All data processing is local (no cloud upload)
- ⚡ **Fast Performance** - Analyzes large procurement datasets in seconds

## Architecture

### Technology Stack

- **Framework**: NW.js (Node Webkit)
- **Runtime**: Node.js + Chromium Embedded Framework (CEF)
- **UI**: Vanilla HTML5, CSS3, JavaScript
- **Excel Engine**: SheetJS/XLSX library
- **Deployment**: Single executable + HTML UI file

### How It Works

```
1. User provides PO Data Excel file
2. Application parses Excel (multi-format support)
3. Data is normalized and validated
4. Analysis algorithms calculate metrics
5. Interactive dashboard displays results
6. User exports findings to formatted Excel
```

## Features

### Data Input
- Accepts Excel (.xlsx, .xls, .xlsm) and CSV files
- Automatic column detection (handles multiple naming conventions)
- Drag-and-drop file import
- Comprehensive data validation

### Analysis Capabilities
- **Vendor Comparison**: Track spending by supplier
- **Price Ladder**: See cheapest, middle, highest supplier per category
- **Cost Variance**: Identify price differences across buyers
- **Type Analysis**: Group and compare by material type/size
- **Savings Calculation**: Quantify potential cost savings
- **Alternative Pricing**: Compare with competing suppliers

### Reporting
- Dashboard with KPIs (quantity, overpayment, savings)
- Summary tables by type and material
- Article-by-article comparison
- Cross-buyer usage analysis
- Formatted Excel export with styling
- Interactive dropdowns in reports

### User Interface
- Responsive design (works on all screen sizes)
- Light and dark theme support
- Keyboard navigation
- Accessible forms and controls
- Real-time filtering and calculations

## Installation

### For Users

1. Download `SourcingCostIntelligence.zip`
2. Extract to a folder (e.g., `Documents\SourcingCostIntelligence`)
3. Right-click `SourcingCostIntelligence.exe` → Create shortcut
4. Double-click shortcut to launch
5. Or drag an Excel file onto the EXE to open with data

**First Run**: May take 1-2 minutes while antivirus scans the application.

### For Developers

1. Clone this repository
2. Modify `index.html` as needed
3. Test in your browser or with NW.js
4. To build executable: Use NW.js build tools with your updated files

## Usage

### Basic Workflow

1. **Launch Application**
   ```
   Double-click SourcingCostIntelligence.exe
   ```

2. **Load Data**
   - Drag Excel file onto window, or
   - Click "Choose file" button
   - Select your PO Data export

3. **Select Analysis Parameters**
   - Choose supplier to review
   - Select comparison suppliers
   - Filter by buyer (optional)
   - Filter by material type (optional)

4. **Review Results**
   - Dashboard shows total bought, overpayment, savings
   - Type table shows summary by material type
   - Article table shows item-by-item comparison
   - Price ladder shows supplier ranking

5. **Export Report**
   - Click "Download Excel" for current view
   - Click "Download Buyer Report" for comprehensive analysis
   - Files open automatically in Excel

### Column Requirements

The application requires these columns in your data:
- **Vendor** (or Supplier, Supplier Name, Mill)
- **Total Value USD** (or Amount USD, PO Value)
- **Total Qty (Primary)** (or Qty, Quantity, Order Qty)

Optional columns for richer analysis:
- Classification / Category / Type
- Material Name / Description
- Specifications / Width / Size
- Color
- Reference Number / Article Number
- Ultimate Buyer / Customer Name
- PO Date

## Data Privacy

✅ **100% Local Processing**
- All data stays on your computer
- No internet connection required
- No data sent to cloud services
- Excel files are not modified
- No tracking or telemetry

## Performance

- File load time: < 2 seconds (after first start)
- Analysis calculation: < 1 second (typical dataset)
- Memory usage: 200-400 MB
- Maximum dataset: 100K+ rows tested

## Supported File Formats

### Input
- Excel 2007+ (.xlsx)
- Excel 97-2003 (.xls)
- Excel Macro-Enabled (.xlsm)
- CSV (Comma-Separated Values)

### Output
- Excel (.xlsx) with multiple sheets and formatting

## Technical Specifications

See [TECHNICAL_SPECS.md](./docs/TECHNICAL_SPECS.md) for detailed information about:
- Build process and dependencies
- Architecture and data flow
- Performance characteristics
- Known limitations and workarounds
- Troubleshooting guide

## Development

### Modifying the Application

The application source code is in `index.html`. To customize:

1. Open `index.html` in a text editor (VS Code recommended)
2. Modify HTML structure, CSS styling, or JavaScript logic
3. Save the file
4. Replace the original `index.html` with your modified version
5. Restart the application to see changes

### Key JavaScript Functions

```javascript
parse(wb)           // Parse Excel workbook
loadFile(file)      // Load and validate file
render()            // Render all visualizations
setupSelectors()    // Initialize UI dropdowns
exportExcel()       // Generate Excel report
```

### Adding New Features

Examples of extensions you could add:
- New analysis metrics
- Additional export formats
- Custom filtering options
- Data visualization charts
- Integration with other systems

## Building from Source

To build a new executable:

1. Install NW.js SDK
2. Prepare your `index.html`
3. Use NW.js builder:
   ```bash
   nwjs-builder-phoenix --output your-app.exe
   ```
4. Package with `index.html` and documentation

## Troubleshooting

### "The Excel reader did not load"
- Check that SheetJS is loaded
- Verify file format is correct
- Reload the application

### "Missing columns" Error
- Verify your Excel has required columns
- Check column names match expected names (see aliases in code)
- Try renaming columns to standard names

### Slow First Start
- Windows/antivirus may be scanning the EXE
- This is normal; subsequent starts are faster
- Add to antivirus whitelist to skip scanning

### Excel Shows Grey/Empty Window
- Try: View menu → Unhide
- Or: Close and re-open file from Downloads folder

### File Drag-and-Drop Not Working
- Ensure `index.html` is in the same folder as EXE
- Try using "Choose file" button instead

## Contributing

If you'd like to contribute improvements:

1. Fork this repository
2. Create a feature branch
3. Make your changes to `index.html`
4. Test thoroughly
5. Submit a pull request

## License

[Specify your license - e.g., MIT, Apache 2.0, Proprietary]

## Support

For issues or questions:
- Check the troubleshooting section above
- Review the inline comments in `index.html`
- Open an issue on GitHub

## Changelog

### v1.0.0 (Current)
- Initial release
- Excel file parsing with multi-format support
- Supplier comparison analysis
- Price ladder analysis
- Cross-buyer variance detection
- Excel report export
- Dark mode support
- Responsive UI

## Project Status

✅ Stable - Production ready

## Acknowledgments

- Built with [NW.js](https://nwjs.io/)
- Excel parsing by [SheetJS](https://sheetjs.com/)
- Modern UI with semantic HTML5

## Related Documents

- [Technical Specifications](./docs/TECHNICAL_SPECS.md)
- [Architecture Overview](./docs/ARCHITECTURE.md)
- [User Guide](./docs/HOW-TO-USE.md)

---

**Last Updated**: November 10, 2026
