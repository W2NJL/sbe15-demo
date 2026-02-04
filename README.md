# FM Signal Strength Prediction: Why Distance Alone Fails

**SBE NYC Chapter 15 Plus Meeting Demo Notebook**

Created by Nick Langan, W2NJL | Villanova University

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/W2NJL/sbe15-demo/blob/main/SBE_FM_Signal_Prediction_Demo.ipynb)

---

An interactive Python notebook exploring why predicting FM radio signal strength requires more than just measuring distance from the transmitter. Using real FCC station data and actual Longley-Rice propagation model results from [RadioLand](https://radiolandapp.com), this notebook demonstrates:

1. **The Haversine formula** for calculating distances between coordinates
2. **A naive distance+power model** and why it fails
3. **Actual Longley-Rice predictions** showing terrain's dramatic impact on signal propagation
4. **Visualizations** comparing simple predictions vs. terrain-aware reality

## The Punchline

The Empire State Building FM stations (WCBS-FM, WNYC-FM, WPLJ) broadcast with 5-7 kW of power from 400+ meters HAAT, only ~38 miles from Sparta, NJ. A simple model predicts ~60 dBu. Longley-Rice says ~25 dBu. The Appalachian foothills block the path entirely.

## Requirements

No local setup needed - just click "Open in Colab" above. The notebook uses only standard Python libraries:
- `math`
- `pandas`
- `matplotlib`
