# Project Holiday

## Opdrachten

### Opdracht 1 - Database ontwerp

- Maak op basis van onderstaande userstories en het SQL-bestand een database ontwerp. 

### Opdracht 2 - Repository

- Maak gebruik van de repository: https://github.com/NOVA-college-Haarlem/holiday-project-blok-3
- Fork de repository
- Clone de repository

### Opdracht 3 - Website

- Maak een website voor een vakantiebestemmingen.

### Opdracht 4 - Controleren

- Controleer je website door gebruik te maken van de rubric.

## Userstories

### Overzichtspagina

**Als een** reiziger  
**Wil ik** een interactieve kaart zien met alle beschikbare vakantiebestemmingen  
**Zodat ik** visueel kan zien waar de bestemmingen zich bevinden

**Als een** reiziger  
**Wil ik** een quick-view kunnen openen van elke bestemming door er met mijn muis overheen te gaan  
**Zodat ik** snel een voorproefje krijg zonder de pagina te verlaten

**Als een** reiziger  
**Wil ik** een favorietenlijst kunnen maken van bestemmingen die mij interesseren  
**Zodat ik** later gemakkelijk terug kan naar mijn interesses

## Filtering

**Als een** reiziger  
**Wil ik** kunnen filteren op reisseizoen (zomer, winter, lente, herfst)  
**Zodat ik** bestemmingen vind die ideaal zijn voor mijn gewenste reisperiode

**Als een** reiziger  
**Wil ik** kunnen filteren op reisduur (weekend, week, twee weken, etc.)  
**Zodat ik** bestemmingen vind die passen bij mijn beschikbare tijd

## Overige Functionaliteiten

**Als een** reiziger  
**Wil ik** kunnen sorteren op reiservaring (avontuurlijk, ontspannend, cultureel)  
**Zodat ik** bestemmingen vind die passen bij mijn reisstijl

**Als een** reiziger  
**Wil ik** een vergelijkingstool kunnen gebruiken om verschillende bestemmingen naast elkaar te zetten  
**Zodat ik** een weloverwogen keuze kan maken

**Als een** bezoeker  
**Wil ik** de tekstgrootte van de website kunnen aanpassen (klein, normaal, groot)  
**Zodat ik** de tekst leesbaar hou

## SQL-bestand

-- Database schema voor vakantiebestemmingen met één tabel

```sql
-- Bestemmingen tabel
CREATE TABLE bestemmingen (
    id INT PRIMARY KEY AUTO_INCREMENT,
    naam VARCHAR(100) NOT NULL,
    land VARCHAR(100) NOT NULL,
    continent VARCHAR(50) NOT NULL,
    vakantietype VARCHAR(50) NOT NULL,
    beschrijving TEXT,
    prijs DECIMAL(10, 2),
    thumbnail_url VARCHAR(255)
);

-- Voorbeelddata invoegen
INSERT INTO bestemmingen (naam, land, continent, vakantietype, beschrijving, prijs, thumbnail_url) VALUES 
('Barcelona', 'Spanje', 'Europa', 'Stad', 'Prachtige stad aan de Middellandse Zee met unieke architectuur van Gaudí.', 599.99, 'barcelona.jpg'),
('Bali', 'Indonesië', 'Azië', 'Strand', 'Tropisch eiland met prachtige stranden, rijstvelden en een rijke cultuur.', 1299.99, 'bali.jpg'),
('Kaapstad', 'Zuid-Afrika', 'Afrika', 'Stad', 'Stad omringd door natuur met de iconische Tafelberg.', 899.99, 'kaapstad.jpg'),
('New York', 'Verenigde Staten', 'Noord-Amerika', 'Stad', 'Wereldstad die nooit slaapt met iconische wolkenkrabbers.', 1499.99, 'newyork.jpg'),
('Rio de Janeiro', 'Brazilië', 'Zuid-Amerika', 'Strand', 'Stad bekend om het Christusbeeld, Copacabana strand en carnaval.', 1199.99, 'rio.jpg'),
('Sydney', 'Australië', 'Oceanië', 'Stad', 'Bruisende stad met het beroemde Opera House en prachtige stranden.', 1799.99, 'sydney.jpg'),
('Rome', 'Italië', 'Europa', 'Cultuur', 'De eeuwige stad met het Colosseum, Vaticaan en prachtige pleinen.', 649.99, 'rome.jpg'),
('Bangkok', 'Thailand', 'Azië', 'Cultuur', 'Levendige hoofdstad met tempels, drijvende markten en heerlijk straatvoedsel.', 999.99, 'bangkok.jpg'),
('Marrakech', 'Marokko', 'Afrika', 'Cultuur', 'Kleurrijke stad met medina, souks en een rijke geschiedenis.', 749.99, 'marrakech.jpg'),
('Vancouver', 'Canada', 'Noord-Amerika', 'Natuur', 'Moderne stad omringd door bergen en oceaan.', 1099.99, 'vancouver.jpg'),
('Cusco', 'Peru', 'Zuid-Amerika', 'Avontuur', 'Historische Incastad op grote hoogte, toegangspoort tot Machu Picchu.', 1299.99, 'cusco.jpg'),
('Auckland', 'Nieuw-Zeeland', 'Oceanië', 'Natuur', 'Grootste stad van Nieuw-Zeeland tussen twee havens.', 1599.99, 'auckland.jpg'),
('Parijs', 'Frankrijk', 'Europa', 'Stad', 'De lichtstad met iconische Eiffeltoren, Louvre en romantische boulevards.', 699.99, 'parijs.jpg'),
('Kyoto', 'Japan', 'Azië', 'Cultuur', 'Traditionele Japanse stad met prachtige tempels en bamboe bossen.', 1399.99, 'kyoto.jpg'),
('Zanzibar', 'Tanzania', 'Afrika', 'Strand', 'Paradijselijk eiland met azuurblauwe zee en witte zandstranden.', 1099.99, 'zanzibar.jpg');
```

# Beoordelingscriteria Vakantiebestemmingen Project

## Overzichtspagina

| Criterium                          | Onvoldoende                                    | Voldoende                                       | Goed                                                                            |
| ---------------------------------- | ---------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------------- |
| **Basisweergave van bestemmingen** | Bestemmingen worden niet of nauwelijks getoond | Bestemmingen worden correct weergegeven         | Bestemmingen worden aantrekkelijk weergegeven met duidelijke visuele hiërarchie |
| **Filter op continent**            | Filter werkt niet of met ernstige fouten       | Filter werkt, maar heeft kleine gebreken        | Filter werkt perfect en is gebruiksvriendelijk                                  |
| **Filter op vakantietype**         | Filter werkt niet of met ernstige fouten       | Filter werkt, maar heeft kleine gebreken        | Filter werkt perfect en is gebruiksvriendelijk                                  |
| **Sortering op prijs**             | Sortering werkt niet of met ernstige fouten    | Sortering werkt, maar heeft kleine gebreken     | Sortering werkt perfect en is gebruiksvriendelijk                               |
| **Doorklikken naar detailpagina**  | Links werken niet of met ernstige fouten       | Links werken, maar zijn niet optimaal geplaatst | Links werken perfect en zijn intuïtief                                          |

## Detailpagina

| Criterium                           | Onvoldoende                               | Voldoende                          | Goed                                                   |
| ----------------------------------- | ----------------------------------------- | ---------------------------------- | ------------------------------------------------------ |
| **Weergave van bestemming details** | Details worden niet of nauwelijks getoond | Details worden correct weergegeven | Details worden uitgebreid en aantrekkelijk weergegeven |
| **Teruglink naar overzichtspagina** | Link werkt niet of is niet aanwezig       | Link is aanwezig en werkt          | Link is duidelijk zichtbaar en gebruiksvriendelijk     |

## Algemene aspecten

| Criterium              | Onvoldoende                                        | Voldoende                                                                  | Goed                                                                      |
| ---------------------- | -------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Database connectie** | Query's werken niet of met ernstige fouten         | Query's werken, maar zijn niet geoptimaliseerd                             | Query's werken goed en zijn geoptimaliseerd                               || **Responsief ontwerp** | Website werkt niet op verschillende schermgroottes | Website werkt op verschillende schermgroottes, maar heeft kleine problemen | Website is volledig responsief en werkt uitstekend op alle schermgroottes |
| **Code kwaliteit**     | Rommelige code met veel fouten                     | Redelijk nette code met enkele fouten                                      | Nette, goed gestructureerde code zonder fouten                            |

## Beoordeling

De beoordeling wordt gebaseerd op de volgende niveaus:
- **Onvoldoende**: Het project voldoet niet aan de basisvereisten
- **Voldoende**: Het project voldoet aan de basisvereisten
- **Goed**: Het project voldoet aan alle vereisten en toont extra aandacht voor gebruikerservaring en code kwaliteit
