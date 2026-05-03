ELASTICSEARCH VJEŽBA

*Opis:Ovaj repozitorij sadrži rješenje vježbe iz kolegija koje uključuje rad s Elasticsearchom i Kibanom.
U projektu su prikazani osnovni koraci rada: pokretanje okruženja, kreiranje indeksa, unos podataka, izvođenje upita i agregacija.

*Pokretanje okruženja:Za pokretanje projekta potrebno je imati instaliran Docker i Docker Compose.
1.Otvoriti terminal u root folderu projekta
2.Pokrenuti sljedeću naredbu:
docker compose up -d
3.Nakon pokretanja:
Elasticsearch je dostupan na: http://localhost:9200
Kibana je dostupna na: http://localhost:5601
U Kibani otvoriti Dev Tools za izvršavanje upita

*Struktura repozitorija:

-docker-compose.yml # konfiguracija za pokretanje Elasticsearch i Kibana servisa

-odgovori.md # pisani odgovori na teorijska pitanja iz zadataka

-queries.json # svi upiti korišteni u zadacima (match, term, range, bool, agregacije)

-README.md # upute za pokretanje i opis projekta

-screenshots/ # screenshotovi rezultata iz Kibane i terminala