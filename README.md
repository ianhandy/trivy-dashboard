# Trivy Dashboard

A beautiful, zero-dependency web UI for visualizing [Trivy](https://github.com/aquasecurity/trivy) security scan results. Drop in a `trivy --format json` output and get an interactive dashboard with severity breakdowns, package grouping, CVSS scores, and scan-to-scan comparison.

![Trivy Dashboard](https://img.shields.io/badge/trivy-dashboard-E5591C?style=for-the-badge)

## Features

- **Drag & drop** or paste Trivy JSON output
- **Severity breakdown** — visual cards and stacked bar for CRITICAL/HIGH/MEDIUM/LOW
- **Two views** — flat table (sortable) or grouped by package
- **Multi-target support** — filter by scan target (OS packages, language deps, etc.)
- **Search & filter** — find specific CVEs, packages, or descriptions
- **Scan comparison** — load a second report to see new/fixed vulnerabilities
- **Export** — download as self-contained HTML or print to PDF
- **Zero dependencies** — single HTML file, runs entirely in the browser
- **FunForrest palette** — dark theme with gold/orange accents

## Usage

### Quick Start

```bash
# Generate a Trivy JSON report
trivy image --format json -o report.json myapp:latest

# Open the dashboard
open index.html
# Drop report.json onto the page
```

### Compare Scans

1. Load your current scan
2. Scroll to "Compare with Previous Scan"
3. Drop your previous scan's JSON
4. See new vulnerabilities and fixes at a glance

### Export

- **HTML** — self-contained shareable report (no server needed)
- **PDF** — use the Print/PDF button for a clean printable layout

## Compatibility

Supports Trivy JSON output from v0.50+. Handles both `Results` array format and legacy formats.

## License

MIT
