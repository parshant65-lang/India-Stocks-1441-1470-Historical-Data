# India-Stocks-1441-1470-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1441 to 1470)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1441-1470-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1441 to 1470)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1441 | `KAUSHALYA` | Kaushalya Infrastructure Development Corporation Limited | `KAUSHALYA.NS` |
| 1442 | `KAVDEFENCE` | Kavveri Defence & Wireless Technologies Limited | `KAVDEFENCE.NS` |
| 1443 | `KAYA` | Kaya Limited | `KAYA.NS` |
| 1444 | `KCP` | KCP Limited | `KCP.NS` |
| 1445 | `KCPSUGIND` | KCP Sugar and Industries Corporation Limited | `KCPSUGIND.NS` |
| 1446 | `KDDL` | KDDL Limited | `KDDL.NS` |
| 1447 | `KDGREEN` | KD Green Industries Limited | `KDGREEN.NS` |
| 1448 | `KECL` | Kirloskar Electric Company Limited | `KECL.NS` |
| 1449 | `KEEPLEARN` | DSJ Keep Learning Limited | `KEEPLEARN.NS` |
| 1450 | `KELLTONTEC` | Kellton Tech Solutions Limited | `KELLTONTEC.NS` |
| 1451 | `KENNAMET` | Kennametal India Limited | `KENNAMET.NS` |
| 1452 | `KERNEX` | Kernex Microsystems (India) Limited | `KERNEX.NS` |
| 1453 | `KESORAMIND` | Kesoram Industries Limited | `KESORAMIND.NS` |
| 1454 | `KEYFINSERV` | Keynote Financial Services Limited | `KEYFINSERV.NS` |
| 1455 | `KHADIM` | Khadim India Limited | `KHADIM.NS` |
| 1456 | `KHAICHEM` | Khaitan Chemicals & Fertilizers Limited | `KHAICHEM.NS` |
| 1457 | `KHAITANLTD` | Khaitan (India) Limited | `KHAITANLTD.NS` |
| 1458 | `KHANDSE` | Khandwala Securities Limited | `KHANDSE.NS` |
| 1459 | `KICL` | Kalyani Investment Company Limited | `KICL.NS` |
| 1460 | `KILITCH` | Kilitch Drugs (India) Limited | `KILITCH.NS` |
| 1461 | `KINGFA` | Kingfa Science & Technology (India) Limited | `KINGFA.NS` |
| 1462 | `KIOCL` | KIOCL Limited | `KIOCL.NS` |
| 1463 | `KIRANVYPAR` | Kiran Vyapar Limited | `KIRANVYPAR.NS` |
| 1464 | `KIRIINDUS` | Kiri Industries Limited | `KIRIINDUS.NS` |
| 1465 | `KIRLFER` | Kirloskar Ferrous Industries Limited | `KIRLFER.NS` |
| 1466 | `KIRLOSIND` | Kirloskar Industries Limited | `KIRLOSIND.NS` |
| 1467 | `KIRLPNU` | Kirloskar Pneumatic Company Limited | `KIRLPNU.NS` |
| 1468 | `KISSHT` | OnEMI Technology Solutions Limited | `KISSHT.NS` |
| 1469 | `KITEX` | Kitex Garments Limited | `KITEX.NS` |
| 1470 | `KJMCFIN` | KJMC Financial Services Limited | `KJMCFIN.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream KAUSHALYA 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1441-1470-Historical-Data/main/KAUSHALYA/1m/2026/10/KAUSHALYA_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
