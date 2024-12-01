# Air vs Rail Travel Time Analysis in European Cities

**Project Work Plan**  
**Group 66: Anabel Dautovic, Ralf Prinz, Wendelin Potz, Hedda Fiedler**  
**December 1, 2024**

---

## Objective
This project investigates travel times between European cities using air and rail transportation. The goal is to identify:
- How travel times compare between rail and air.
- Which connections are faster by train than by air.
- Connections that could become faster by train if high-speed rail were implemented.
- The most and least well-connected cities based on travel times.

---

## To-Do List
### Now:
- [ ] Improve the rail network filtering so it doesn’t take forever to load.
- [ ] Implement dataset saving to minimize loading times
    - maybe chunk dataset to keep code from crashing 
- [ ] Merge rail and air data
- [ ] come up with sanity checks ?

### Later:
- [ ] Create isochrone maps to show connectivity.
- [ ] rankings for most/least connected cities.
- [ ] Pull everything into the presentation/report.
- [ ] Add high-speed rail travel time estimates.

---

## Methodology
### Question Refinements:
1. Focus on cities with populations ≥ 500K.
2. Analyze only direct flight connections.
3. Use fixed transit times for both air and rail.

### Steps:
1. Calculate travel time estimates for rail and air for each city pair.
2. Compare journey times and identify routes where `rail time ≥ air time`.
3. Recalculate travel times for rail using a theoretical high-speed rail speed (300 km/h) and identify newly competitive routes.
4. Determine connectivity metrics and rank cities based on the number of minimum-time connections.
5. Visualize the connectivity with isochrones.

---

## Data Sources
### City Data:
- **EUROSTAT Population Database**  
  [View Dataset](https://ec.europa.eu/eurostat/databrowser/view/urb_cpop1/default/table?lang=en)
- **City Coordinates from OpenDataSoft**  
  [Explore Dataset](https://public.opendatasoft.com/explore/dataset/geonames-all-cities-with-a-population-1000)

### Air Travel:
- **European Airports IATA Codes**  
  [Dataset](https://www.kaggle.com/datasets/rusiano/european-airports-iata-codes)
- **Airport Database with Coordinates**  
  [Details](https://www.partow.net/miscellaneous/airportdatabase/)
- **Flight Route Database (7 years old)**  
  [Dataset](https://www.kaggle.com/datasets/open-flights/flight-route-database)
- **European Flights Dataset**  
  [Dataset](https://www.kaggle.com/datasets/umerhaddii/european-flights-dataset)

### Rail Travel:
- **Train Station Data from Kaggle**  
  [Dataset](https://www.kaggle.com/datasets/headsortails/train-stations-in-europe)
- **OpenStreetMap Rail Network Data via OSMnx**  
  [OpenRailwayMap](https://www.openrailwaymap.org/)

### Additional Resources:
- **EU Transport Analysis**  
  [EU Report](https://ec.europa.eu/regional_policy/sources/work/2023-rail-vs-air_en.pdf)
- **Transit Time Research Paper**  
  [The Open Transportation Journal](https://opentransportationjournal.com/VOLUME/13/PAGE/48/FULLTEXT/)

- **OSMnx Examples Gallery**
    [Git] (https://github.com/gboeing/osmnx-examples/tree/main)

---

## Current Status
### Data Preparation:
- **City Data:** 80 cities identified using EUROSTAT and OpenDataSoft.
- **Air Travel:** Direct flight connections mapped. Travel times calculated using the haversine formula and integrated with average transit times.
- **Rail Travel:** Initial OSMnx implementation tested for rail network visualization. Scaling and optimization are ongoing.

---

## Work Distribution
| **Task**                     | **Team Member(s)**                  |
|-------------------------------|--------------------------------------|
| Gathering air travel data     | Anabel                              |
| Gathering rail travel data    | Ralf, Hedda                         |
| Comparative analysis          | Ralf                                |
| Visualization                 | Wendelin                            |
| Setting up shared environment | Wendelin                            |
| Presentation and report       | Hedda                               |

---

## Planned Deliverables
1. Comparative analysis of rail vs. air travel times.
2. Visualization of travel time competitiveness using isochrones.
3. Rankings of city connectivity based on minimum-time connections.
4. Final presentation and report.

---