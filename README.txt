# Japan Influenza–Temperature Analysis

This project analyzes the relationship between ambient temperature and influenza activity in Japan using **WHO FluNet** and **Open-Meteo** data.

The project is developed as part of a Data Science PBL I course.

## Project Focus

The analysis explores:

- the relationship between weekly temperature and influenza activity,
- seasonal patterns of influenza activity,
- whether temperature decreases tend to occur before influenza activity increases,
- recurring influenza patterns across multiple years.

## Data Sources

### WHO FluNet

FluNet provides weekly influenza surveillance data for Japan.

The project currently considers two possible definitions of influenza activity:

1. **Influenza positivity rate**
   - Positive influenza specimens divided by the number of specimens processed.

2. **Influenza-positive specimen count**
   - Weekly number of influenza-positive specimens reported through FluNet surveillance.

The final definition of influenza activity is still under evaluation.

### Open-Meteo

Historical temperature data are collected from representative locations across Japan.

| Area | Location |
|---|---|
| Hokkaido | Sapporo |
| Tohoku | Sendai |
| Kanto | Tokyo |
| Japan Sea / Hokuriku | Niigata |
| Chubu | Nagoya |
| Kansai | Osaka |
| Chugoku | Hiroshima |
| Shikoku | Takamatsu |
| Kyushu | Fukuoka |
| Subtropical South | Naha |

The weather dataset includes:

- daily mean temperature,
- daily minimum temperature,
- daily maximum temperature.

The selected locations are used to create a **multi-location temperature proxy for Japan**, not an official national average temperature.

## Setup

Create the Conda environment from the provided file:

```bash
conda env create -f requirements.yml
```

Then start JupyterLab:

```bash
jupyter lab
```

## Current Status

FluNet data for Japan have been prepared and audited.

Open-Meteo temperature data have also been collected from the selected locations. Weather preprocessing and auditing are being completed before the influenza and temperature datasets are merged.

The final definition of **influenza activity** and the final **study period** have not yet been selected.

## Data Sources

- WHO FluNet: https://www.who.int/tools/flunet
- Open-Meteo: https://open-meteo.com/