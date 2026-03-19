# Analiza Rynku Nieruchomości - Kraków (OLX Scraper)

## Opis projektu
Automatyczny system pozyskiwania i analizy danych o cenach mieszkań w Krakowie. Projekt obejmuje pełny proces ETL (Extract, Transform, Load): od scrapingu danych z portalu OLX, przez walidację i czyszczenie w Pythonie, po składowanie w relacyjnej bazie danych PostgreSQL i końcową wizualizację w Power BI.

## Wykorzystane technologie
* Python 3.x (Requests, BeautifulSoup4, Pandas, Re)
* PostgreSQL
* Power BI
* Git

## Architektura rozwiązania
1. **Ekstrakcja danych**: Skrypt `scraper.py` pobiera dane z wielu podstron serwisu, omijając dynamiczne zmiany w strukturze HTML poprzez dopasowywanie wzorców tekstowych.
2. **Przetwarzanie (Data Cleaning)**: Wykorzystanie wyrażeń regularnych (Regex) do wyodrębnienia metrażu, dzielnicy oraz czyszczenia cen z błędnych formatowań i jednostek.
3. **Składowanie**: Dane są przesyłane do bazy PostgreSQL w celu zapewnienia spójności i możliwości dalszej analizy SQL.
4. **Wizualizacja**: Interaktywny raport Power BI pozwalający na filtrowanie cen wg dzielnic oraz identyfikację ofert typu 'outlier' (okazje rynkowe).

## Struktura repozytorium
* `/scraper.py` - Kod źródłowy parsera.
* `/schema.sql` - Definicja tabeli w bazie danych.
* `/requirements.txt` - Lista zależności Pythona.
* `/data_sample.csv` - Eksport przykładowych danych.
