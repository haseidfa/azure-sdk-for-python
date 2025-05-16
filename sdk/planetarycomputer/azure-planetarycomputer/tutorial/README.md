
# 🌍 Microsoft Planetary Computer Pro SDK - Getting Started Tutorial

This repository contains a Jupyter Notebook that demonstrates how to interact with the **Microsoft Planetary Computer Pro GeoCatalog** using the official Python SDK.

## 📘 Tutorial Overview

The tutorial walks you through the following steps using SDK **only** (no raw REST calls):

| Step | Description |
|------|-------------|
| 🔐 Authenticate | Authenticate using `DefaultAzureCredential` |
| 🧱 Create Collection | Define and create a STAC collection |
| 🖼️ View Thumbnail | Fetch and render the thumbnail using SDK |
| 📖 Read Collection | Retrieve STAC collection metadata |
| 🔍 STAC Search | Query STAC items by bbox and datetime |
| 📦 Ingest Items | Post STAC items to the collection from a public catalog |
| 🧭 Render Config | Define how imagery should be visualized |
| 🧩 Mosaic Config | Configure how imagery tiles are composed |
| 📊 Ingestion Status | View ingestion operation details |
| 🗑️ Delete Item | Remove individual STAC items |
| 🧹 Delete Collection | Delete the STAC collection |

All steps are validated against the endpoint:
```
https://ppe-ch-2.ceefe5e6ahe2haft.northcentralus.geocatalog.spatio-ppe.azure-test.net
```

---

## 🧪 Requirements

To run the notebook, make sure the following are installed:

```bash
pip install -r requirements.txt
```

### `requirements.txt`

```txt
azure-identity
azure-planetarycomputer
pystac
pystac-client
shapely
Pillow
requests
```

You also need:
- Azure CLI (`az login`)
- Python 3.9+

---

## 🚀 Run the Tutorial

```bash
# Activate your virtual environment
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook PlanetaryComputer_Tutorial_Final.ipynb
```

---

## 🔐 Environment Setup (Optional)

You can optionally configure environment variables in a `.env` file:

```
ENDPOINT=https://ppe-ch-2.ceefe5e6ahe2haft.northcentralus.geocatalog.spatio-ppe.azure-test.net
```

---

## 📂 File Structure

```
sdk/
└── planetarycomputer/
    └── azure-planetarycomputer/
        ├── tutorial/
        │   ├── PlanetaryComputer_Tutorial_Final.ipynb  # ✅ Tutorial notebook
        │   └── README.md
        ├── generated_samples/
        ├── generated_tests/
        ├── setup.py
        ├── requirements.txt
        └── ...
```

---

## 🧼 Notes

- Ensure no SAS tokens or credentials are committed.
- Replace `<PUT_SIGNED_CATALOG_URL_HERE>` and `<PUT_ITEM_ID_HERE>` in the notebook before execution.

