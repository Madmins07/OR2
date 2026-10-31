<div align="center">
  <img src="assets/banner.svg" alt="Baggage Optimisation. Dynamic programming against integer programming for multi-objective packing." width="100%"/>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/python-3.10+-FF7A1A?style=flat-square&labelColor=0A0B0E&logo=python&logoColor=EEF1ED" alt="python 3.10+"/>
  <img src="https://img.shields.io/github/last-commit/Madmins07/OR2?style=flat-square&labelColor=0A0B0E&color=6A7280&label=updated" alt="last-commit"/>
  <a href="https://uditangshu-or2-app-hjvctt.streamlit.app"><img src="https://img.shields.io/badge/live-uditangshu--or2--app--hjvctt.streamlit.app-F4F5F7?style=flat-square&labelColor=0A0B0E" alt="live uditangshu--or2--app--hjvctt.streamlit.app"/></a>
</div>

## about

Course project for **IM21204 Operations Research II** at IIT Kharagpur. The problem: a student is moving and has to
decide which items go in **cabin baggage**, which go in **check-in baggage**, and which get shipped through
**packers and movers**, subject to weight and volume limits, item compatibility, and cost. It is a multi-objective
knapsack with three bins.

We formulated it two ways and compared them:

- **Dynamic programming**, with an efficiency score blending value per kilogram and value per litre.
- **Integer programming** in PuLP, solving the exact model.

The report covers the formulations, the trade-off between solution quality and runtime, and sensitivity to the
value-weight and value-volume ratios. A group submission; the hosted Streamlit app is deployed from a teammate's account.

## inside

| file | what it does |
|:--|:--|
| `packing_optimizer.py` | Both formulations, the comparison harness, and a CLI run over the sample data. |
| `app.py` | Streamlit interface: upload your own item sheet, set limits and costs, see the allocation and charts. |
| `data/dorm_items.xlsx` | Sample item sheet: a typical Indian college student's dorm inventory. |
| `docs/OR_Report.pdf` | Full write-up with the LaTeX formulations and results. |

## run

```bash
pip install -r requirements.txt
streamlit run app.py              # interactive app
python packing_optimizer.py       # runs DP and IP on data/dorm_items.xlsx and prints the comparison
```

---

<div align="center">
  <sub>Part of <a href="https://github.com/Madmins07">Madmins07</a> · Madhav Agarwal · IIT Kharagpur</sub>
</div>
