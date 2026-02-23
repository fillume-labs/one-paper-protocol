# One Paper Protocol (OPP)

**The immutable evidence layer for global collaboration.**

> "Data follows the paper, not the system."

---

## 📖 Introduction
In traditional B2B workflows, data is often trapped in siloed systems, leading to high trust costs and fragmented evidence. **One Paper Protocol (OPP)** decouples the "Ground Truth" from application logic. It treats every business action as a digital "sheet of paper"—immutable, portable, and self-contained.

## 🛠 The S.T.R.P. Framework
We define the lifecycle of business evidence into four atomic stages:

* **`s` (Submit)**: Capturing the truth. Minimalist interface for immutable evidence capture (Photos, Geo-location, Timestamp).
* **`t` (Track)**: The flow of trust. A unified standard for identifying and tracing "digital sheets" across entities.
* **`r` (Report)**: Aesthetic clarity. Aggregating fragmented evidence into human-readable, high-fidelity reports.
* **`p` (Pay)**: Value closure. Defining rules for value exchange triggered by verified facts.

## 🚀 Why OPP?
* **System Agnostic**: Data exists independently of the ERP/WMS. No more vendor lock-in.
* **Evidence-First**: Built-in support for cryptographic proof and physical environment metadata.
* **Minimalist Integration**: Zero-heavy-lifting. Integrate via a simple URL-based protocol.

## 📂 Protocol Specification (v1.0 Alpha)
The core of OPP is a structured JSON object that contains both the **Evidence** and the **UI Logic**.

```json
{
  "protocol": "OPP/1.0",
  "id": "opp_sheet_unique_id",
  "metadata": {
    "timestamp": "2026-02-23T15:00:00Z",
    "issuer": "fillume.tech",
    "proof": {
       "type": "image",
       "url": "https://s.1paper.link/e/xyz",
       "hash": "sha256..."
    }
  },
  "body": {
    "title": "Warehouse Snap Receipt",
    "nodes": [
      {
        "type": "field",
        "id": "n1",
        "label": "Package ID",
        "value": "PKG-99281",
        "style": "bold"
      },
      {
        "type": "field",
        "id": "n2",
        "label": "Weight",
        "value": "12.5kg",
        "unit": "kg"
      },
      {
        "type": "status",
        "id": "n3",
        "label": "Condition",
        "value": "Good",
        "theme": "success"
      }
    ]
  }
}
