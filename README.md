# GS1 / Digital Product Passport Demo

**Landing page:** https://refgerty.github.io/GS1/dpp/BAT-1KWH-DEMO.html  
**GS1 Digital Link:** https://refgerty.github.io/GS1/01/09506000134352/21/00001/

## Structure
```
/dpp/BAT-1KWH-DEMO.html         # human-friendly landing with embedded JSON-LD
/01/09506000134352/21/00001/index.html    # GS1 Digital Link redirect to /dpp/BAT-1KWH-DEMO.html
/passports/dpp_passport_refgerty.json # raw JSON-LD (optional)
.nojekyll                         # required for GitHub Pages to serve /01/... folders
```

## Add a new SKU
1. Duplicate `/dpp/BAT-1KWH-DEMO.html` → `/dpp/<SKU>.html` and update the JSON-LD inside.  
2. Create `/01/<GTIN14>/21/<SERIAL>/index.html` with a meta-refresh redirect to the new `/dpp/<SKU>.html`.  
3. Commit & push. The QR target is: `.../01/<GTIN14>/21/<SERIAL>/`.

## Notes
- Carbon footprint value for this demo: **1.41244 kg CO₂e / unit (0.45 kg)** from openLCA (ELCD 3.2, IPCC 2013 GWP 100a).  
- Demo limitations: electrolyte & graphite not modelled; replace with supplier EPD or ecoinvent data for production.
