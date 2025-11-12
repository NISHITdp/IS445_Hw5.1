---
layout: default
title: HW5 — Jekyll + Altair (UFO)
---

# IS 445 — HW5

**Data:** [UFO sightings (time-standardized)](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)  
**Notebook:** (add your GitHub page-view link to `hw5_altair_export.ipynb` after pushing)

## Plot A — Linked time brush → state counts
<iframe src="charts/ufo_time_state.html" width="100%" height="460" style="border:0;"></iframe>

## Plot B — Lat/Long scatter with shape filter
<iframe src="charts/ufo_map_shape.html" width="100%" height="520" style="border:0;"></iframe>

---

## Write-up

### Plot A
**What:** monthly UFO sighting counts with top US states.  
**Design:** area chart (`month:T`×`size:Q`) + bar chart (`state:N`×`count():Q`).  
**Transforms:** timestamp parsing, monthly aggregation, filter to US.  
**Interactivity:** interval brush on the time series filters the state bars.

### Plot B
**What:** geographic spread of sightings by shape.  
**Design:** circle marks (`longitude`×`latitude`) with conditional color.  
**Transforms:** numeric lat/long conversion + drop nulls.  
**Interactivity:** dropdown selection bound to `shape` highlights points.
