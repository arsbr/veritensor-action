# Veritensor GitHub Action

Add AI Supply Chain & RAG Security to your CI/CD pipeline in 2 lines of code. 
Veritensor scans Models (`.pkl`, `.pt`), Datasets (`.parquet`), Notebooks, and Documents for Prompt Injections, PII Leaks, and Malware.

## Usage (Open Source / Local Scan)

This configuration runs the lightweight Python CLI directly in your GitHub Actions runner.

```yaml
steps:
  - uses: actions/checkout@v4
  
  - name: Scan AI Artifacts
    uses: arsbr/veritensor-action@v1
    with:
      target: '.'
      generate-html: 'true'
```

## Enterprise Usage (Hybrid Scan)

If you have deployed the Veritensor Enterprise Control Plane (Air-Gapped Docker containers), you can route heavy files to your internal servers for deep ML analysis (DeBERTa, GLiNER, YARA, EasyOCR).

```Yaml
steps:
  - uses: actions/checkout@v4

  - name: Enterprise Scan
    uses: arsbr/veritensor-action@v1
    with:
      target: '.'
      report-to: 'https://veritensor.yourcompany.internal/api/v1/telemetry'
      api-key: ${{ secrets.VERITENSOR_API_KEY }}
```
