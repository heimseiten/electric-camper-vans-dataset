# Electric Camper Vans Dataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24224008.svg)](https://doi.org/10.5281/zenodo.24224008)

An open, sourced dataset of 44 electric campers, camper conversions and conversion kits (price, status and steering per market, range, battery, dimensions, berths, caveats), maintained by [EV Camper Guide](https://www.evcamper.guide/).

- `evcampers.json`: full dataset, one object per model with `markets`, `specs`, `sources`, `caveats`
- `evcampers-markets.csv`: flat table, one row per model and market with key specs and source URL
- Live source: https://www.evcamper.guide/data/evcampers.json (mirrored from the live site)

## Main fields
`id, name, converter{name,country,url}, base{make,model,variant}, drivetrain, body, kind (camper/kit/...), status_overall, markets[{market,status,price{amount,currency,incl_vat,from,as_of},steering,source}], specs{battery_kwh,range_km,range_cycle,dc_kw,ac_kw,power_kw,length_mm,width_mm,height_mm,seats,berths,weight_kg,payload_kg,...}, spec_sources, highlights, caveats, sources[{url,title,publisher,date}], last_checked, verification{checked,state}`. `fx` holds the ECB reference rates used for euro conversion.

## Source principle
Every price and spec points to a public source URL (`sources`, indexed by `source` / `spec_sources`). `null` means unknown, never zero.

## Differences from the live file
Image and video references are removed. Everything else is identical.

## License
[CC BY 4.0](LICENSE). Attribution required: credit "EV Camper Guide" and link to https://www.evcamper.guide/ .

## Cite
EV Camper Guide. *Electric Camper Vans Dataset* (2026). https://www.evcamper.guide/ , https://github.com/heimseiten/electric-camper-vans-dataset (CC BY 4.0). DOI: https://doi.org/10.5281/zenodo.24224008 . See `CITATION.cff`.
