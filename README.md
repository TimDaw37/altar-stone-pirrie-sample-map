# Pirrie et al. 2026 - sample and comparison locality map

**Citation (use exactly):** Pirrie, D., Bevins, R.E., Ixer, R.A., Pearce, N.J.G. et al. 2026. Searching for the origin of the Stonehenge Altar Stone: new sedimentological, petrographical, mineralogical, geochemical and isotopic constraints. Journal of the Geological Society 183(6). https://doi.org/10.1144/jgs2026-090 (published online 5 Nov 2026).
Supplementary data (CC BY 4.0): https://doi.org/10.6084/m9.figshare.c.8736920 (one file, `jgs2026-090_si_001.xlsx`).

## Licence

Map and locality data by Tim Daw, licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Quoted paper text is short quotation for commentary. The static map basemap is [Natural Earth](https://www.naturalearthdata.com/); the interactive map uses [OpenStreetMap](https://www.openstreetmap.org/copyright) tiles.

## The main finding (read this first)

This paper does **not** report new field samples, and neither the paper nor the SI gives any coordinates, grid references or latitude/longitude for any locality.
- The only new material analysed is **museum samples of the Altar Stone itself** (MS1-MS3 and five others in Table 1), which have no field locality.
- The "comparison localities" are **regional ORS basins/areas**, tested against *published or unpublished datasets from other studies* (Bevins 2020/2023a/2024, Saßnowski 2015, McKellar 2020, Morton 2021, Leng 1999 and so on). They appear in the text, and in Figs 1a and 11 as labelled basin outlines.
- The SI tables hold only Altar Stone data (pXRF, AMICS, XRPD, O/C and Sr-Sm-Nd isotopes, colour). Table S2's "LOCATION" column is just the analysis group (Altar Stone wet/dry analyses, debitage fragment, "Wilts 277" = Salisbury Museum 2010K.240).

So the map can only show **basin-scale, approximate** positions. No individual sample site exists to plot, and none was invented.

## Files

| File | What |
|---|---|
| `map.png` | Static map (Natural Earth basemap, matplotlib, OSGB). Colour = the paper's conclusion; citation on the map. |
| `index.html` / `map.html` | Leaflet map (OSM tiles), popups with ID / formation / tests / conclusion / source; links open in a new tab; citation in footer. Needs internet for tiles and the Leaflet CDN. `index.html` is the GitHub Pages entry point. |
| `localities.csv` | All 37 records (mapped, reference, museum, unmapped), with source and `approx_flag`. |
| `localities.geojson` | The 11 approximate areas (outline + marker each) and Stonehenge. |

## Counts

- **Mapped: 11 comparison areas, all approximate (0 exact)** - C01-C11. Plus Stonehenge as a reference point (R01), which is not a sample locality.
- **Museum samples: 8** (M01-M08), no field locality, not mapped (listed in an inset/note and in the CSV).
- **Unmapped comparison areas named in the text: 17** (U01-U17).

## Method

1. **Sources read:** the published paper and its CC BY 4.0 supplementary data, including all nine SI tables and Table 1 for the museum samples. Every quoted phrase in the CSV was checked against the paper text.
2. **Conclusions** are taken only from the paper's text (quoted or closely paraphrased, with the section in `paper_location_of_evidence`). Classes: EXCLUDED; PARTLY EXCLUDED; OPEN (not excluded in paper); CONTRADICTORY IN PAPER (the text does not consistently exclude or keep the area open); NO CONCLUSION IN PAPER (labelled or Ba anomaly only); REFERENCE. The paper's overall conclusion is that no examined outcrop matches and the provenance "has yet to be determined with confidence", so there is no "match" class.
3. **Georeferencing of Fig. 11** (the paper's UK ORS / stream-sediment Ba map): the figure's black coastline outline was fitted to the Natural Earth coastline by a similarity transform in OSGB (EPSG:27700), optimised by distance-transform matching (mean residual about 2 km on the coast; the Stonehenge icon in the figure falls about 1 km from the real monument). The tan ORS outcrop polygons were segmented by colour, then each was assigned to the nearest labelled basin. The marker is the area-weighted centroid of that label's polygons. Because the polygons are schematic and partly hidden under the Ba overlay, treat positions as good to **about 10-20 km**.
4. **Approximate flag:** all 11 mapped rows have `approx_flag = TRUE`, `mapped_status = approximate`, a diamond marker, and a dashed outline. Stonehenge is a star.
5. **Stonehenge coordinates** (51.1789 N, 1.8262 W) are not in the paper or SI. A standard published position was used as the georeferencing control point and reference marker.
6. **Unmapped:** anything named only by place or unit (Caithness, Tarbat Peninsula, Foula/Shetland, Stonehaven Group, Pennine Basin Carboniferous and so on) has no coordinates or figure position and was **not** placed on the map from its name. Shetland appears only in a separate-scale inset in Fig. 11, so it was not georeferenced. The Lake District is labelled but its outcrop is too small to resolve.

## Source of each locality

| ID | Mapped as | Source |
|---|---|---|
| C01-C11 (Orkney, Orcadian Basin, Midland Valley, Lanark Basin, Fintona, Curlew Mts, Dingle, Peel, Anglesey, Anglo-Welsh Basin, North Devon) | **Approximate**, from Fig. 11 labels/outcrops (Fig. 1a shows the same labels). Tests/conclusions from the text sections cited in the CSV. | Paper Fig. 11, Fig. 1a, Provenance discussion |
| R01 Stonehenge / in-situ Altar Stone | Reference | Paper (location shown on Figs 1, 11); SI Tables S1, S2 (in-situ pXRF) |
| M01-M08 museum samples | Not mapped | Paper Table 1; SI Tables S2, S4-S9 for MS1-MS3 |
| U01-U17 | Unmapped | Paper text |

Tests run on the museum samples (SI): pXRF (S1, S2), AMICS automated SEM-EDS (S3-S5), XRPD whole-rock and clay (S6), O/C isotopes of calcite (S7), Sr-Sm-Nd (S8, MS1 and MS2 only), colour (S9), plus CL and SEM for MS1.

## Gaps and caveats

- No site-level coordinates exist in the paper or SI; this is a basin-level map. Site-level points would have to come from the cited source papers (Bevins 2020, 2023a, 2024; Saßnowski 2015; McKellar 2020; Phillips 2009; Hillier 2006) and be added as a separate layer with its own citation.
- Several comparison datasets the paper relies on are unpublished or "in prep." (Pembrokeshire zircon, Fig. 12c; CZi from 32 Pembrokeshire samples) and have no locality information.
- Fig. 11 hides parts of the ORS outcrop beneath the Ba overlay, so polygons are incomplete (notably Lanark and parts of the Orcadian Basin).
- Possible inconsistency inside the paper: Table 1 lists zircon dating only for SH08 FN593, but the text says Clarke et al. (2024) dated zircon, apatite and rutile from MS3 and 2010K.240 (and FN593). The CSV records the text's version for M01/M07 and Table 1 for the others.
- Midland Valley Basin (C03) is classed as CONTRADICTORY IN PAPER: the Petrography and sedimentology section (citing Phillips 2007) excludes the Silurian–Devonian ORS of that basin, but the Heavy mineral suite section leaves the Scottish Midland Valley a possible source in the absence of modern heavy-mineral data, and the zircon discussion discounts only the NE Midland Valley overlying ORS (plus the southern-margin Silurian sandstones), noting that 'There have been no zircon U–Pb studies of the ORS elsewhere in the Midland Valley'. The Abstract and Conclusions do not name the Midland Valley. The specific NE and southern-margin units (U06–U08) remain EXCLUDED.
- "Lanark Basin" is classed as no conclusion because the text mentions it only for a Ba anomaly. Whether the Midland Valley statements (themselves inconsistent; see C03) were meant to cover it is not stated.
- The Orcadian Basin (C02) record merges sub-areas with different outcomes (Caithness excluded on clay, Moray Firth discounted on heavy minerals, Shetland partly open); see U01-U03, U16 for the detail.
