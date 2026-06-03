# Data Dictionary - Bluestock Mutual Fund Analytics

## Table 1: fact_nav (NAV History)
| Column | Data Type | Description |
|--------|-----------|-------------|
| Scheme | TEXT | Name of mutual fund scheme |
| Code | INTEGER | AMFI scheme code |
| Date | DATE | NAV date |
| NAV | FLOAT | Net Asset Value |

## Table 2: dim_fund (Fund Master)
| Column | Data Type | Description |
|--------|-----------|-------------|
| schemeCode | INTEGER | Unique scheme code |
| schemeName | TEXT | Full name of scheme |

## Table 3: fact_live_nav (Live NAV)
| Column | Data Type | Description |
|--------|-----------|-------------|
| Scheme | TEXT | Name of mutual fund scheme |
| Code | INTEGER | AMFI scheme code |
| Date | DATE | Latest NAV date |
| NAV | FLOAT | Latest Net Asset Value |

## Data Sources
- nav_history: mfapi.in API - last 30 days
- fund_master: mfapi.in API - scheme list
- live_nav: mfapi.in API - latest NAV
