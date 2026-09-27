# Methodology: Japanese Manufacturing Sites in Poland

**v0.1 · Analysis: September 2026**

This analysis connects verified manufacturing locations with Poland's high-speed-road infrastructure. The current dataset supports analytical outputs and development of the methodology; it is not an exhaustive or statistically representative census.

## 1. Manufacturing-site definition

The GIS master dataset uses one row per distinct geographical manufacturing site associated with a Japanese company in Poland. Manufacturing scope includes verified production and steel-processing operations.

A company, a geographical site and an individual facility are different units. A company may operate several geographical sites. Several buildings or production facilities at the same site do not automatically create additional site records. An office or company listing alone is insufficient evidence of a manufacturing site.

## 2. Site discovery and verification

Initial candidates were assembled primarily from company lists, including the Japanese business/chamber member list. Company and official information were used to review manufacturing activity and the geographical location of each site. Candidate discovery is separate from verification: membership or inclusion on a list does not itself establish a manufacturing operation.

The current master contains 19 sites accepted through project review. “Verified” describes this review status, not independent certification. Source links and source-check dates remain incomplete for some records; strengthening the supporting documentation is part of continued dataset development. This release does not claim a fresh independent verification of every source.

## 3. Geographic coordinates

Address-based geocoding provides candidate coordinates, which are reviewed before inclusion in the site dataset. A geocoding match alone does not prove that manufacturing takes place at that location.

A recorded site point represents a location, not a surveyed property boundary or necessarily a verified vehicle gate. For road access, it is associated with a nearby road-network origin. The connection between the recorded point and that origin is not included in the reported distance and may require further verification.

## 4. Geographic sources and A/S high-speed-road network

A-class roads are motorways and S-class roads are expressways. The geographic sources have distinct roles:

- **Administrative boundaries:** Państwowy Rejestr Granic (PRG), Główny Urząd Geodezji i Kartografii (GUGiK), accessed via Geoportal. PRG data were processed for GIS analysis and provide administrative-boundary context in the map.
- **Map background and road-network analysis:** © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright). OpenStreetMap provides the map/background data. Its road data were processed to identify Polish A- and S-class high-speed roads and calculate road-network accessibility. Both the public A/S road layer and the road-access calculations use OSM geometry. OSM data is available under the Open Database License (ODbL).
- **Official road reference:** Generalna Dyrekcja Dróg Krajowych i Autostrad (GDDKiA). Its motorway and expressway reference layers, accessed via Geoportal, were used for visual/reference validation of the A/S road network. They are not rendered in the public map and do not supply the geometry for the public A/S road layer or routing calculations.

The analysis distinguishes the main high-speed carriageway from the approach roads and entrance ramps. Road geometry alone does not establish that a driver can enter the high-speed road: network connectivity, direction of travel and mapped access conditions also matter. The results reflect the available data snapshot rather than live road conditions.

## 5. A/S road-access-distance definition

**A/S road access distance is the road-network distance from a manufacturing site to a legal entry point onto an A- or S-class high-speed road.**

Operationally, the reported distance follows the drivable network from the site's associated road-network origin, along ordinary roads and entrance ramps, to a permitted mainline entry in either direction. It seeks the shortest distance under the current model and its assumptions. It excludes the connection from the site point to the network origin and any onward journey along the A/S road.

Results use passenger-car access assumptions. They do not establish suitability for heavy goods vehicles, travel time, congestion, or accessibility toward a particular destination. Access from within a factory may depend on vehicle authorization; a calculated result is not a declaration that private factory roads are publicly accessible.

Straight-line proximity can differ from legal road access, which is why the analysis uses road-network distance.

## 6. Quality assurance

Quality review separates site identity and manufacturing evidence from coordinate quality and route validity. It considers whether site locations are plausible, whether a route connects to an A/S mainline, and whether mapped travel directions and access conditions support the result.

Results are presented as:

- **Calculated (10 sites):** an accepted result under the current model. This does not mean all origin permissions or real-world conditions have been independently confirmed.
- **Under review (9 sites):** the current routing and verification model cannot confidently determine a valid result. No distance is assigned for public interpretation.

An unresolved result is not zero distance, evidence of poor access, or proof that no real-world route exists. Further review may resolve missing or ambiguous network information and site-access conditions.

## 7. Current limitations

- **Coverage:** the 19 verified sites are an initial, non-exhaustive dataset influenced by the candidate sources used. They do not support population-level conclusions.
- **Documentation:** some supporting source links and verification dates are incomplete.
- **Origins:** site points and their road-network origins may differ from actual vehicle exits; the intervening connection is excluded from the metric.
- **Permissions:** factory access can require authorization, and mapped information may not establish actual gate access.
- **Network information:** missing, outdated or ambiguous road connections and restrictions can affect both calculated and unresolved results.
- **Vehicle scope:** passenger-car assumptions cannot be generalized to trucks or specialist transport.
- **Timing and precision:** distances are estimates for the available snapshot, not live navigation instructions or survey measurements. Rounded map labels do not imply greater accuracy.

Dataset expansion, stronger source documentation and review of remaining access results will inform future versions.

[Return to the project overview](../README.md).
