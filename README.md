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

## Kontrollista: så vet du att du är klar

- [ ] Varje formulärfält har en etikett som är kopplad med `for`/`id`.
- [ ] Rätt `type` används: e-post är `email`, telefon är `tel`, datum är `date`.
- [ ] Kryssrutor och radioknappar ligger i `fieldset` med `legend`.
- [ ] Obligatoriska fält har `required` och syns som obligatoriska för användaren.
- [ ] Du kan fylla i hela formuläret med enbart tangentbordet.
- [ ] Båda sidorna validerar utan fel.
- [ ] Filerna är uppladdade till din fork och länken är inskickad.

## Tips om du fastnar

- Klick på etiketten gör ingenting? Då är `for` och `id` inte identiska (stor/liten bokstav räknas).
- Radioknapparna går att välja flera av? De behöver exakt samma `name`.
- Placeholder är inte en etikett! Den försvinner när man skriver och läses inte alltid upp.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Reflektion: Förklara med egna ord varför en `placeholder` inte kan ersätta en `label`.

## Vill du mer? (frivilligt)

- Lägg till `<input type="number">` för barnstolar med `min="0"` och `max="5"`.
- Lägg till `aria-describedby` på e-postfältet som pekar på ett hjälpstycke.
