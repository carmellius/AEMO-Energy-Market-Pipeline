This folder documents the end-to-end data pipeline architecture from data ingestion to analytics and visualization.

## Pipeline Overview

This project evaluated three data ingestion approaches for AEMO NEM analytics.

### Pipeline A: NEMWEB
Direct ingestion of AEMO published dispatch files.
Pros: authoritative, complete.
Cons: heavy preprocessing, inconsistent formats.

### Pipeline B: OpenElectricity API
API-based access to NEM data.
Pros: clean abstraction.
Cons: API instability during beta, unreliable responses.

### Pipeline C: NEMOSIS (Selected)
Python library providing structured access to AEMO MMS tables.
Pros: reproducible, structured, analyst-friendly.
Cons: learning curve.

Pipeline C was selected for final analysis.
