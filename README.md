# Veritensor GitHub Action

Add AI Supply Chain & RAG Security to your CI/CD pipeline in 2 lines of code.

## Usage

```yaml
steps:
  - uses: actions/checkout@v4
  
  - name: Scan AI Artifacts
    uses: arseniibrazhnyk/veritensor-action@v1
    with:
      target: '.'
      generate-html: 'true'
```
Enterprise Usage (Hybrid Scan)
```Yaml
- name: Enterprise Scan
    uses: arsbr/veritensor-action@v1
    with:
      report-to: 'https://veritensor.yourcompany.internal/api/v1/telemetry'
      api-key: ${{ secrets.VERITENSOR_API_KEY }}
```
