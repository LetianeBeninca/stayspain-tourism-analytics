# StaySpain: Tourism Demand & Revenue Strategy Analysis

Team project from the business simulation of the **IT Academy Data Analytics bootcamp** (Barcelona Activa), October–November 2025.
The team acted as the data analytics department of **StaySpain**, a fictional company that manages tourist accommodation in eight Spanish destinations, and answered weekly business questions from the Operations, Customer Experience and Marketing teams. In the last week the internal data was combined with public demand statistics from the Spanish National Statistics Institute (INE).

**Stack:** Python (pandas, scikit-learn, matplotlib, seaborn), MySQL, Power BI.

## Team (Equipo 19)

Done together with my teammates from the simulation:

- Letiane Benincá
- Anabel Martínez Ramírez
- Borja Munitiz
- Irene Nieves Miranda
- Andres Vidal Monge

**My contribution (Letiane):** I worked with Anabel on the UX / data-visualization side of the project: designing the charts and dashboards, building the storytelling around the proposal, and contributing to the analyses behind it.

## What was done

| Week | Focus | Notebooks | Dashboard (PDF) |
|---|---|---|---|
| 1 · 27 Oct | Data understanding, cleaning, first exploratory analysis | `notebooks/week1_2025-10-27/` | `dashboards/week1_…` |
| 2 · 3 Nov | Updated dataset, missing-value strategy, customer experience (best vs worst rated), amenity feature importance (Random Forest) | `notebooks/week2_2025-11-03/` | `dashboards/week2_…` |
| 3 · 10 Nov | Price vs satisfaction by city, neighbourhood optimization potential, outlier capping | `notebooks/week3_2025-11-10/` | `dashboards/week3_…` |
| 4 · 17 Nov | External demand data (INE, 2015–2021): seasonality of visits, average overnight stays, country of residence, traveller-profile clustering | `notebooks/week4_2025-11-17/` | `dashboards/week4_…` |

Each weekly folder follows the same order: `01` data cleaning → `02` exploratory analysis (EDA) → `03` to `05` the business question of each team (operations, customer experience, marketing). SQL sanity checks of each dataset are in `sql/`.

## Repository structure

```
notebooks/    Weekly analyses (Jupyter), in Spanish and Catalan as written during the course
sql/          Sanity checks run on the MySQL database
dashboards/   Power BI dashboards exported to PDF, one per week
data/ine/     Public INE tables: travellers and overnight stays in tourist apartments, 2015–2021
data/derived/ Aggregated outputs used in the dashboards
docs/         Data understanding document (week 1)
```

## Data

- **Internal data (StaySpain).** A dataset of tourist accommodation listings (about 9,400 listings in Barcelona, Madrid, Mallorca, Girona, Valencia, Málaga, Sevilla and Menorca) provided by the bootcamp through a private MySQL database. **The listing-level CSV files are not included in this repository.** The notebooks read the data from that database; see "Running the notebooks".
- **External data (INE).** Travellers and overnight stays in tourist apartments by province, month and country of residence, 2015–2021, from the Spanish National Statistics Institute ([INEbase](https://www.ine.es/dyngs/INEbase/operacion.htm?c=Estadistica_C&cid=1254736176962&menu=resultados&idp=1254735576863#_tabs-1254736195412)). `..` in the tables means "not significant". The country of residence includes aggregates (Total, Non-residents in Spain, European Union excluding Spain). Source: INE.

## Running the notebooks

The week 1–3 notebooks connect to the course MySQL database, which is no longer needed to read the results. The notebooks keep the saved outputs. To re-run them against your own copy of the data, set the environment variables `DB_HOST`, `DB_USER` and `DB_NAME`; the password is asked at run time. Credentials are not stored in the notebooks.

## Notes

- The analyses were written during the course. Some notebooks contain absolute local paths from the original machines and mixed Spanish/Catalan/English comments; they were kept as run.

## License

Code and notebooks are released under the [MIT License](LICENSE). The INE tables in `data/ine/` keep their original source and terms (INE, cite the source).

## Context

Part of my data portfolio. See also: [IT Academy bootcamp exercises](https://github.com/LetianeBeninca/it-academy-data-analytics) and [PhD thesis: building optimization](https://github.com/LetianeBeninca/phd-thesis-building-optimization).
