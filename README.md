# PAnalytics Zenodo Archive

This private GitHub repository manages the automated preparation and upload of academic files (PDFs, CSVs) to [Zenodo](https://zenodo.org/), under the `panalytics` community.

## 📁 Folder Structure

```
pdf/             → All PDF files to upload (named by DOI)
metadata/        → Matching JSON metadata files (from CSV wizard or manual prep)
scripts/         → Python automation scripts
upload_log.csv   → Auto-generated upload tracker
```

## ⚙️ Core Features

- ✅ Batch upload to Zenodo via API
- ✅ DOI deduplication with skip logic
- ✅ 7-day rate limiting (customizable)
- ✅ Dry-run mode and logging
- ✅ Metadata extraction from CSV (via `csv_to_json_metadata.py`)

## 🚀 Getting Started

1. Create a virtual environment:
   ```
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

2. Set your Zenodo token:
   ```
   export ZENODO_TOKEN=your_token_here
   ```

3. Run the uploader:
   ```
   python scripts/upload_batch_to_zenodo.py
   ```

## 🧪 Development Notes

- All uploads are logged to `upload_log.csv`
- Metadata must be validated before submission
- Scripts support both manual and automated workflows

---

© Managed by Eric McLamore and contributors.