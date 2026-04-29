<div align="center">

# 🟣 RigPK

**PCPartPicker for Pakistan**

Browse PC parts from Pakistani retailers, build your own rig, check compatibility, and explore prebuilt systems — all in one place.

[![Backend](https://img.shields.io/badge/backend-rigpk--backend-7c3aed?style=flat-square)](https://github.com/AzaanFaisal606/rigpk-backend)
[![Frontend](https://img.shields.io/badge/frontend-rigpk--front-7c3aed?style=flat-square)](https://github.com/AzaanFaisal606/rigpk-front)
[![License](https://img.shields.io/badge/license-MIT-7c3aed?style=flat-square)](https://github.com/AzaanFaisal606/rigpk-backend/blob/master/LICENSE)

</div>

---

## What Is This?

Pakistan has no dedicated PC part price aggregator. Buyers manually check 5–6 retailer sites, compare prices, and guess at compatibility. RigPK fixes that.

It scrapes prices from major Pakistani PC retailers daily, stores them with history, and surfaces everything through a fast, filterable interface — plus a PC builder that tells you when parts are incompatible before you buy.

---

## Features

- 🛒 **Parts Market** — ~4,800 parts across GPU, CPU, RAM, SSD, PSU, case, motherboard, and cooling
- 🔧 **PC Builder** — pick components slot by slot with live compatibility warnings
- 🔗 **Shareable Builds** — generate a short link to share your build with anyone
- 🖥️ **Prebuilt Browser** — 121 prebuilt PCs filterable by price, CPU brand, and GPU brand
- 📊 **Price History** — every scrape run is logged; price trends tracked over time

---

## How It Works

```
Retailers → Python Scrapers → SQLite DB → FastAPI → Next.js Frontend
```

Scrapers fetch product pages from each retailer using plain `urllib` — no headless browser required. Product specs (socket type, VRAM, DDR generation, wattage, etc.) are extracted automatically from product names using regex rules, so no manual tagging needed.

---

## Retailers Covered

### Parts (~4,800 products)

| Retailer | Categories |
|---|---|
| czone.com.pk | GPU, CPU, RAM, SSD, PSU, Case, Motherboard, Cooling |
| zahcomputers.pk | GPU, CPU, RAM, SSD, PSU, Case, Motherboard, Cooling |
| junaidtech.pk | GPU, CPU, RAM, SSD, PSU, Case, Motherboard, Cooling |
| amdhouse.pk | GPU, CPU, RAM, SSD, PSU, Case, Motherboard, Cooling |
| rbtechngames.com | GPU, CPU, RAM, SSD, PSU, Case, Motherboard, Cooling |

### Prebuilt PCs (121 systems)

| Retailer | Systems |
|---|---|
| zestrogaming.com | 28 |
| redtech.pk | 20 |
| techmatched.pk | 73 |

---

## Planned Features

- 🤖 **AI Build Wizard** — describe your use case and budget, get a recommended build
- ✅ **Full Compatibility Checking** — PSU wattage, RAM slots, case form factor, cooler clearance
- 📈 **Price History Graphs** — visualize price trends per part over time
- 👤 **User Accounts** — save builds, track wishlisted parts, get price drop alerts
- 🏪 **User Marketplace** — list and browse used PC parts for sale

---

## Repositories

| Repo | Description |
|---|---|
| [rigpk-backend](https://github.com/AzaanFaisal606/rigpk-backend) | Python scrapers, SQLite DB, FastAPI REST API |
| [rigpk-front](https://github.com/AzaanFaisal606/rigpk-front) | Next.js 16 frontend — market, builder, prebuilts |

---

## Tech

**Backend:** Python · FastAPI · SQLite · urllib

**Frontend:** Next.js 16 · TypeScript · Framer Motion

---

<div align="center">
Built by <a href="https://github.com/AzaanFaisal606">Azaan Faisal</a> · MIT License
</div>
