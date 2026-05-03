### Zadatak 1
- green — svi shardovi su aktivni, sve radi normalno
- yellow — primarni shardovi rade, ali replica shardovi nisu dostupni
- red — neki primarni shardovi nisu dostupni, podaci mogu biti nedostupni

### Zadatak 2
- naslov je text jer želimo full-text pretragu (riječi, dijelovi teksta)
- naslov.keyword postoji za točne usporedbe, sortiranje i agregacije
- autor i zanr su keyword jer se koriste za točno filtriranje i grupiranje
- opis nije keyword jer bi tada bio jedna vrijednost i ne bi se mogao pretraživati po riječima

### Zadatak 3
- 'cuprija' pronalazi 'ćuprija' zbog asciifolding filtera (uklanja dijakritike)
- _score predstavlja relevantnost dokumenta (koliko dobro odgovara upitu)
- razlikuje se jer neki dokumenti imaju više podudaranja ili važnije riječi

### Zadatak 5
Tokeni: na, drini, cuprija
- lowercase pretvara tekst u mala slova
- asciifolding uklanja dijakritike (ć → c)
- Analyzer je ključan jer omogućuje da pretraga radi nad riječima i njihovim varijacijama.
Bez njega bi pretraga bila točna i nefleksibilna (morala bi se poklapati 100%).

Elasticsearch je brži od SQL LIKE '%tekst%' jer koristi invertirani indeks.
Omogućuje naprednu analizu jezika (npr. uklanjanje dijakritika).
Rezultati su rangirani po relevantnosti (_score), dok SQL vraća samo podudaranja.
Podržava fuzzy pretragu i sinonime.
Skalira se horizontalno (više servera).
SQL LIKE je spor jer mora skenirati cijelu tablicu.
Elasticsearch je optimiziran za full-text search.