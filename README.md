# 834 Enrollment Analyzer

A browser-based utility for exploring ANSI X12 834 enrollment files (implementation guide target: 005010X220A1). It parses the file in the browser and presents enrollment summaries, member-level details, segment/loop views, and downloadable exports.

## Features

- Reads `.edi`, `.x12`, `.txt`, and other text-based X12 files
- Detects element and segment delimiters from the ISA header
- Summarizes employees, dependents, active/terminated status, plans, maintenance types, relationships, and coverage levels
- Provides member search and filtering
- Displays parsed X12 segments and loop labels
- Exports member data and plan summaries to CSV, enrollment data to JSON, and a simplified XML representation
- Includes synthetic sample data for demonstration
- Runs as a static page with no build step or server required

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Select a synthetic or approved test EDI file, or click **Load sample 834**.

No package installation or build process is required.

## 🚀 Live Demo

**[Open the 834 Enrollment Analyzer](https://amritraj-edi.github.io/834-enrollment-analyzer/)**

Try the browser-based tool to inspect sample X12 834 enrollment data, explore member and segment details, and export analysis results.

> **Note:** Use synthetic sample data for demonstrations. This tool is intended for portfolio and learning purposes; it is not a certified X12 compliance validator or a production enrollment-processing system.

## Privacy and data handling

The page's own implementation reads the selected file through the browser File API and processes it with local JavaScript. The code does not include an EDI upload request, a backend endpoint, or an AI API integration. Export files are generated through browser download APIs.

The page does not load third-party web fonts; it uses system fonts. As with any web application, hosting configuration, browser extensions, endpoint security software, and the surrounding environment are outside the scope of this static HTML file. Verify network activity and follow your organization's security/privacy requirements before using sensitive data.

**Use synthetic data for public demos and screenshots. Do not commit real member data, production EDI files, generated exports, credentials, or other confidential information to GitHub.** This project is a demonstration utility, not a certified EDI validator or a substitute for production enrollment controls.

## Known limitations

- The parser implements a focused set of common 834 segments and fields; it is not a complete X12 implementation.
- Loop assignment and interpretation are heuristic and may not cover every trading-partner companion guide or variation.
- It should not be treated as a replacement for payer/carrier validation, companion-guide rules, reconciliation, or production QA.
- Review all extracted values and counts against trusted source systems before making business decisions.
- The generated XML is a simplified conversion format, not an official X12-to-XML standard mapping.

## Suggested portfolio description

**834 Enrollment Analyzer — Browser-Based EDI Utility**  
Built a standalone JavaScript tool to parse ANSI X12 834 enrollment files and surface member, coverage, plan, and maintenance summaries. Added member-level search/filtering, segment inspection, and CSV/JSON/XML exports to make enrollment data easier to review. Designed the demo to process file contents locally in the browser without a backend upload or AI API integration.

Tailor this description to your actual contribution and be ready to explain the parser's scope and limitations in an interview.

## Suggested resume bullet

- Developed a browser-based ANSI X12 834 enrollment analyzer using HTML, CSS, and JavaScript, with member/coverage summaries, segment-level inspection, searchable records, and CSV/JSON/XML exports.

## Repository hygiene

Before publishing:
- Use only the synthetic sample included in the tool.
- Check the repository for client names, member identifiers, real EDI files, and confidential screenshots.
- Review the code and test exports with representative synthetic files.
- Add screenshots only after ensuring they contain no real or sensitive data.
