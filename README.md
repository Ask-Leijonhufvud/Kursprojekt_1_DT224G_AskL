# Kursprojekt 1 DT224G

Detta är en liten webbplats med lite information om några av de datorspel som jag spelar, t.ex.:
- Vad det går ut på;
- Vad jag gillar om det; 
- Vad jag inte gillar om det; 
- Hur mycket jag spelat spelet vid det tillfälle jag skrev webbsidan.

## Vilka tekniker har använts?

HTML och CSS

## Länkar till publicerade versioner

* [GitHub Pages](https://ask-leijonhufvud.github.io/Kursprojekt_1_DT224G_AskL/)
* [Miun Webbhost](sftp://asle2601@studenter.miun.se/userhome/asle2601/public_html/dt224g_ask_leijonhufvud)

## Frågor och svar

### Vad är skillnaden mellan `git add` och `git commit`?

`git commit` lägger till en uppsättning ändringar till repot, medans `git add` förbereder en ändrad fil för att commitas.

### Varför avänder man branches istället för att jobba direkt i main?

En anledning kan vara för att - om man har ett flertal medarbetare som alla arbetar med olika delar av ett projekt samtidigt - förhindra att medarbetare av misstag skriver över varandras arbete genom att alla arbetar i sina egna grenar istället för main.

En annan anledning kan vara för att man har satt upp en branch där man testar en funktion eller liknande innan man gör den tillgänglig för allmänheten, och main är den branch som är vad allmänheten ser, t.ex. om webbplatsen automatiskt uppdateras när main uppdateras.

### Vad händer rent praktiskt när man gör en merge?

(För enkelhetens skull kallar vi härefter grenen från vilken man mergar för mottagar-grenen och grenen som man namnger i merge-kommandot för mål-grenen)

Antingen - om inga commits gjorts i mottagar-grenen sedan mål-grenen separerades - Flyttas helt enkelt HEAD för mottagar-grenen till HEAD för mål-grenen.

Annars skapas en ny commit, en merge-commit, i mottagar-grenen, som slår samman alla commits i båda grenar sedan de separerades. Om samma sak ändrats i båda grenar måste man manuellt välja vilken grens version som man vill ha kvar.

### Vad är skillnaden mellan att pusha till GitHub och att publicera direkt på t.ex. Netlify?

När man pushar till GitHub uppdaterar man helt enkelt online-repot till att matcha det som förvaras lokalt på ens dator, men när man publicerar på t.ex. Netlify skapas en faktisk webbplats.

### Om du vill exkludera någon fil i projektet från versionshanteringen, hur gör du då?

Man lägger till filen i repots `.gitignore`-fil