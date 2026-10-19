# Dag 2 · Formulär och tillgänglig markup

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du bygger bokningsformuläret på `kontakt.html` så att det fungerar för alla, även den som använder tangentbord eller skärmläsare.

## Bakgrund

Ett formulär är ofta det viktigaste en webbplats gör: det är där användaren faktiskt *gör* något. Ett fält utan koppling till sin etikett (`label`) är oanvändbart för många. Idag lär du dig koppla rätt, välja rätt `type` och gruppera rätt. Du börjar med din färdiga startsida från igår (den är med i repot).

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Läs igenom kontakt.html

Filen har skelettet och kommentarer med `TODO`. Texterna till fälten finns i `innehall.md`.

### Steg 2. Bygg de vanliga fälten

Skapa fälten för namn, e-post, telefon och datum. Varje fält är en `<div class="falt">` med en `<label for="...">` och en `<input>` vars `id` är samma som `for`. Välj rätt `type`: `text`, `email`, `tel`, `date`. Lägg på `name` och `autocomplete` där det passar.

### Steg 3. Lägg till rullista och textfält

Antal personer är en `<select>` med `<option>`. Övriga önskemål är en `<textarea>` med egen etikett.

### Steg 4. Gruppera val med fieldset

Kostönskemål (kryssrutor) och bekräftelsesätt (radioknappar) ligger i var sin `<fieldset>` med `<legend>`. Varje kryssruta/radioknapp har en egen `<label>`. Radioknapparna delar samma `name`.

### Steg 5. Obligatoriska fält och knapp

Markera obligatoriska fält med `required` och med en stjärna i etiketten. Avsluta med en `<button type="submit">`.

### Steg 6. Testa med tangentbordet och musen

Klicka på en etikett: fältet ska få fokus. Tabba genom formuläret utan mus: kommer du åt allt i logisk ordning? Försök skicka tomt formulär: webbläsaren ska klaga på de obligatoriska fälten.

### Steg 7. Validera

Kör både `index.html` och `kontakt.html` genom W3C-validatorn.

## AI-spåret (nivå 1: Förklara och granska)

**Be AI om checklistan, bygg formuläret själv** (cirka 20 minuter, efter att du gjort din egen lösning)

AI är din granskare och förklarare. AI skriver inte din lösning. En bra checklista är mer värd än färdig kod, eftersom du kan använda den på varje formulär du bygger i framtiden.

Regler: egen lösning först, du ska kunna förklara varje rad, och du loggar i `docs/ai-logg.md` i `mitt-projekt`. Reglerna finns i `AI-REGLER.md` i `mitt-projekt`.

1. Be AI om en checklista (utan kod) med prompten nedan.
2. Jämför med ditt eget formulär: vad har du, vad saknas?
3. Rätta luckorna själv. Skriv koden med egna händer.
4. Testa med tangentbordet och med Lighthouse.
5. Skriv i ai-loggen: vilka punkter var nya för dig, och vilka var överdrivna eller fel?

Prompt att utgå från:

```
Lista som checklista vad ett tillgängligt
bokningsformulär måste uppfylla:
etiketter, fälttyper, gruppering,
felmeddelanden och tangentbord.
Ge ingen kod, bara punkter.
```

**Kontrollera med:**

- Klicka på varje etikett: får fältet fokus?
- Fyll i formuläret med bara tangentbordet.
- Kör Lighthouse (Accessibility).

**I ditt projekt:** Gå igenom checklistan på formuläret i ditt projekt.

## Kontrollista: så vet du att du är klar

- [ ] Varje formulärfält har en etikett som är kopplad med `for`/`id`.
- [ ] Rätt `type` används: e-post är `email`, telefon är `tel`, datum är `date`.
- [ ] Kryssrutor och radioknappar ligger i `fieldset` med `legend`.
- [ ] Obligatoriska fält har `required` och syns som obligatoriska för användaren.
- [ ] Du kan fylla i hela formuläret med enbart tangentbordet.
- [ ] Båda sidorna validerar utan fel.
- [ ] Filerna är uppladdade till din fork och länken är inskickad.
- [ ] Du har gjort AI-uppgiften och skrivit en post i `docs/ai-logg.md`.

## Tips om du fastnar

- Klick på etiketten gör ingenting? Då är `for` och `id` inte identiska (stor/liten bokstav räknas).
- Radioknapparna går att välja flera av? De behöver exakt samma `name`.
- Placeholder är inte en etikett! Den försvinner när man skriver och läses inte alltid upp.

## Ditt projekt: Dagens steg i `mitt-projekt`

Efter övningen här jobbar du vidare i ditt eget projekt (din design från modul 3). Dagens steg står i `PROJEKTSTEG.md` i ditt repo `mitt-projekt`, under **Dag 2**. Det är där ditt riktiga arbete växer. Övningen här är träningsbanan.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Länk till ditt `mitt-projekt`.
3. Reflektion: Förklara med egna ord varför en `placeholder` inte kan ersätta en `label`.

## Vill du mer? (frivilligt)

- Lägg till `<input type="number">` för barnstolar med `min="0"` och `max="5"`.
- Lägg till `aria-describedby` på e-postfältet som pekar på ett hjälpstycke.
