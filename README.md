# krakow-halas-gis

Analiza narażenia mieszkańców Krakowa na hałas drogowy za pomocą QGIS

Cel projektu
Identyfikacja obszarów w Krakowie o wysokim natężeniu hałasu drogowego oraz oszacowanie liczby mieszkańców narażonych na jego negatywne działanie na podstawie danych przestrzennych.

Wykorzystane dane
Dane pochodzą z Miejskiego Systemu Informacji Przestrzennej (MSIP) w Krakowie:
- Warstwa punktowa „Zameldowania stałe i czasowe” (dane na dzień 31.12.2023 r.) – zawierająca m.in. liczbę mieszkańców w poszczególnych punktach adresowych/kratkach.
- Warstwa wektorowa „Mapy hałasu 2022 – imisja dróg” (obszary LDWN) – określająca poziom hałasu drogowego w decybelach (dB).

Metodologia
1. Wczytano dane do QGIS i ustawiono układ współrzędnych na EPSG:2180.
2. Odfiltrowano punkty zameldowania do najnowszego okresu (31.12.2023).
3. Wykonano przestrzenne połączenie warstw (Spatial Join – „Złącz atrybuty według lokalizacji”) w celu przypisania do budynków poziomu hałasu.
4. Oczyszczono dane z duplikatów geometrycznych (powstałych na skutek nakładania się stref hałasu na siebie), używając narzędzia do usuwania zduplikowanych geometrii.
5. Wyodrębniono punkty znajdujące się w strefach o podwyższonym natężeniu hałasu (powyżej 60 dB).

Wyniki
Zidentyfikowano 3 840 punktów adresowych, w których zamieszkuje łącznie 527 667 osób narażonych na hałas drogowy przekraczający 60 dB. Wyniki przedstawiono na mapie tematycznej.

Narzędzia: QGIS, analiza przestrzenna, filtrowanie danych, statystyka.



Spatial analysis of traffic noise exposure in Krakow using QGIS

Project Objective
Identification of areas in Krakow with high traffic noise levels and estimation of the number of residents exposed to its negative effects, based on spatial data.

Data Sources
Data was obtained from the Municipal Spatial Information System (MSIP) in Krakow:
- Point layer "Zameldowania stałe i czasowe" (Permanent and temporary registrations, as of 31.12.2023) – containing the number of residents per address point/grid.
- Vector layer "Mapy hałasu 2022 – imisja dróg" (2022 Noise maps – road emission, LDWN areas) – defining the traffic noise level in decibels (dB).

Methodology
1. Data was loaded into QGIS and the Coordinate Reference System was set to EPSG:2180.
2. Registration points were filtered to the most recent period (31.12.2023).
3. A Spatial Join operation was performed to assign the noise level to each building point.
4. The dataset was cleaned of geometric duplicates (caused by overlapping noise zones) using the Delete Duplicate Geometries tool.
5. Points located in zones with elevated noise levels (above 60 dB) were extracted.

Results
Identified 3,840 address points with a total of 527,667 residents exposed to traffic noise exceeding 60 dB. The results are presented on the thematic map.

Tools used: QGIS, Spatial Analysis, Data Filtering, Statistics.
