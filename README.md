# Dual-Site Graphene E-Skin for Respiratory Sensing — ML Analysis

Machine-learning (ML) code and data for the paper:

> **"Layer- and Growth-Dependent Graphene Electronic Skin for Dual-Site Respiratory Sensing"**

Two graphene e-skins on the anterior neck — over the **jugular notch (JN)** and the **laryngeal
prominence (LAR)** — are used to estimate the airflow waveform (regression) and classify breathing
state (classification). Dual-site fusion outperforms either site alone.

---

## Contents

| Archive | Role | Contents |
|---|---|---|
| `Gr_E-skin_Respiratory_Sensor_raw_data_breathe.zip` | Inputs | Raw breath recordings (sensor time-series). |
| `Gr_E-skin_Respiratory_Sensor_scripts.zip` | Code | `replicate_pipeline.py` — preprocessing + ML evaluation. |
| `Gr_E-skin_Respiratory_Sensor_data.zip` | Outputs | Benchmark metrics and feature importances. |

**Flow:** raw recordings → `replicate_pipeline.py` → benchmark metrics.

---

## How to Run

```bash
pip install numpy pandas scipy scikit-learn   # Python 3.9+
python replicate_pipeline.py
```

Set the input path in `replicate_pipeline.py` to the unzipped raw-recordings folder:

```python
DATA_DIR = r"path/to/Gr_E-skin_Respiratory_Sensor_raw_data_breathe"
```

The script pools all three days and reproduces the benchmark metrics (regression and classification).
