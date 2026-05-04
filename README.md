<div align="center">

<img src="https://raw.githubusercontent.com/AzaanFaisal606/rigpk-front/main/public/favicon.svg" width="64" height="64" alt="RigPK logo" />

# RigPK

**PCPartPicker for Pakistan**

Everything in one place, no going from website to website, store to store, looking to upgrade a specific part you have listings of 100s of them, enjoy!.

[![Backend](https://img.shields.io/badge/backend-rigpk--backend-7c3aed?style=flat-square)](https://github.com/AzaanFaisal606/rigpk-backend)
[![Frontend](https://img.shields.io/badge/frontend-rigpk--front-7c3aed?style=flat-square)](https://github.com/AzaanFaisal606/rigpk-front)
[![License](https://img.shields.io/badge/license-MIT-7c3aed?style=flat-square)](https://github.com/AzaanFaisal606/rigpk-backend/blob/master/LICENSE)

</div>

---

## What Is This?

When building my own Geming Rig, I really wished there was a website like PC-Part-Picker for pakistan, so that I wouldn't have to go through the multiple websites of different retailers, some old and slow.
So I decided to build this, take all the part listings and even prebuilts and show them all in one place for users to track/ compare prices.

It scrapes prices from major Pakistani PC retailers daily, stores them with history, and surfaces everything through a fast, filterable interface — plus a PC builder that tells you when parts are incompatible before you buy.
This is meant to be a learning/(why not) project for me, so I will keep adding new Ideas or things im curious to learn. 

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

## Disclaimer

The database is not presistent as of yet, since project is deployed on render free tier, currently I run a fresh scrape at the end of every week on my personal computer, and push the updated databse to the root repo to serve as a default DB, presistant DB and automated scrapes will be implemented soon.

<div align="center">
Built by <a href="https://github.com/AzaanFaisal606">Azaan Faisal</a> · MIT License
</div>
