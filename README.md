# Rule-Based Fraud Detection System

# Bank Statement Fraud Detection System

A user-friendly web application for analyzing bank statements and detecting potentially fraudulent transactions using rule-based detection algorithms.

## Overview

This application provides financial institutions and individuals with a tool to scan bank statements for suspicious activity. It uses a configurable rule-based approach to identify unusual transactions that may indicate fraud.

## Features

- **CSV Upload**: Drag-and-drop or file browser for easy bank statement upload
- **Intelligent Column Mapping**: Automatically maps CSV columns to transaction fields with manual override options
- **Rule-Based Detection Engine**: Analyzes transactions using configurable fraud detection rules
- **Risk Assessment**: Assigns risk scores and categorizes transactions as High, Medium, or Low risk
- **Detailed Analysis**: View comprehensive transaction details and triggered rules
- **Summary Statistics**: Visual dashboard with transaction counts, volumes, and risk distribution
- **Report Export**: Download complete analysis results as CSV

## Fraud Detection Rules

The system implements several detection rules including:

1. **Large Transaction Amount**: Flags transactions above a configurable threshold
2. **Unusual Transaction Hour**: Identifies transactions occurring during suspicious hours (2AM-5AM)
3. **High Transaction Frequency**: Detects multiple transactions in a short timeframe
4. **Geographical Velocity**: Flags transactions in different locations within a short period
5. **Unusual Penny Amounts**: Identifies transactions with uncommon cent values (potential card testing)
6. **New Merchant Category**: Detects transactions in merchant categories not previously used

## How to Use

1. **Upload CSV File**: Drag and drop your bank statement CSV or use the browse button
2. **Map Columns**: The system will attempt to automatically map CSV columns to required fields
   - Verify and adjust mappings as needed
   - Configure user profile settings (like large amount threshold)
3. **Analyze Transactions**: Click the "Analyze Transactions" button
4. **Review Results**: 
   - Transactions are color-coded by risk level
   - Click "View" for detailed information about each transaction
   - Review summary statistics and risk distribution
5. **Download Report**: Click "Download Report" to save results as CSV

## Implementation Details

- Built with vanilla JavaScript, HTML, and CSS
- Uses Bootstrap 5 for responsive UI components
- PapaParse library for CSV parsing
- Chart.js for data visualization
- No server-side component required - all analysis happens in the browser

## Setup Instructions

1. Download all files to your local machine or server
2. Open the HTML file in a modern web browser (Chrome, Firefox, Edge, Safari)
3. No additional setup, installation, or internet connection required after initial load

## CSV Format Requirements

The application works with any CSV bank statement format but requires mapping to these fields:
- Transaction ID (required)
- Date/Time (required)
- Amount (required)
- Location (required)
- Category (required)
- Description (optional)

## Customization

The fraud detection system can be extended with custom rules by modifying the `getDefaultRules()` method in the FraudDetectionSystem class.

## Privacy & Security

All processing is done locally in your browser - no data is sent to any external servers.

## Browser Compatibility

Compatible with all modern browsers. For optimal experience, use the latest version of Chrome, Firefox, Edge, or Safari.
 
## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Inspired by common fraud detection patterns in the financial industry
- Designed for educational and practical implementation purposes
