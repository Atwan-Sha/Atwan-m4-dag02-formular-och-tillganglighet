# Innehåll till bokningsformuläret

**Rubrik:** Boka bord
**Ingress:** Fyll i formuläret så bekräftar vi din bokning inom ett dygn. Fält markerade med * är obligatoriska.

## Fält
| Fält | Etikett | Typ | Obligatoriskt |
|---|---|---|---|
| Namn | Namn * | text | ja |
| E-post | E-postadress * | email | ja |
| Telefon | Telefon (valfritt) | tel | nej |
| Datum | Datum * | date | ja |
| Antal | Antal personer * | select: 1, 2, 3, 4, 5 eller fler | ja |
| Kost | Kostönskemål | kryssrutor: Vegetarisk, Vegansk, Glutenfri | nej |
| Svar | Hur vill du få bekräftelsen? * | radioknappar: E-post, SMS | ja |
| Önskemål | Övriga önskemål | textarea | nej |
| Samtycke | Jag godkänner att Kafé Kardemumma sparar mina uppgifter för bokningen. * | kryssruta | ja |

**Knapp:** Skicka bokning

Sidhuvud och sidfot är desamma som på startsidan. Tips: kopiera från `index.html`. Ändra bara menyn så att den passar sidan.
