# Filtriranje poslodavaca i radnih mjesta

## Opis projekta

Cilj projekta je da se iz postojeće Excel baze izdvoje poslodavci i radna mjesta koja odgovaraju određenim studijskim programima i oblastima interesovanja.

Projekat je namijenjen lakšem pronalaženju potencijalnih poslodavaca za praksu, pripravnički staž i zaposlenje u oblastima analitike podataka, informacionih tehnologija i digitalizacije.

## Korišćene tehnologije

- Python
- Pandas
- Excel

## Kako funkcioniše?

1. Učitava se Excel fajl `pso_poslodavci_pozicije.xlsx` pomoću Pandas biblioteke.
2. Definiše se lista studijskih programa koji odgovaraju traženom obrazovanju.
3. Definiše se lista relevantnih radnih mjesta i oblasti interesovanja.
4. Iz baze se izdvajaju samo redovi koji odgovaraju i studijskom programu i nazivu radnog mjesta.

Rezultati se čuvaju u DataFrame-u `poslodavci_relevantni`.

## Izvoz rezultata

Dobijeni podaci mogu se izvesti u Excel fajl radi lakšeg pregleda i dalje obrade.

```python
poslodavci_relevantni.to_excel('Posalji mejl.xlsx', index=False)
```

## Napomena

Filter koristi tačno poklapanje naziva studijskih programa i radnih mjesta sa vrijednostima iz definisanih lista.
