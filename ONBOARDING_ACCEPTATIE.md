# Onboarding en verplichte acceptatie — [NAAM APP]

**Placeholdergegevens**
- Developer: [NAAM DEVELOPER]
- Contact: [CONTACT E-MAIL]
- Versiedatum: [VERSIEDATUM]
- App: [NAAM APP]

## Tekst vóór gebruik

Lees de [gebruiksvoorwaarden](GEBRUIKSVOORWAARDEN.md) en de [privacyverklaring](PRIVACYVERKLARING.md) voordat je [NAAM APP] gebruikt.

De app is een algemeen hulpmiddel en geen financieel advies, schuldhulpverlening of medische of psychologische zorg. Gebruik de app niet om bankinloggegevens of betaalkaartgegevens op te slaan. In deze versie worden appgegevens lokaal in de browser bewaard; ze kunnen verloren gaan als je browsergegevens wist of van apparaat wisselt. Een account is niet nodig.

## Verplichte checkbox

De gebruiker moet de checkbox zelf aanvinken. Laat deze **standaard uitgevinkt**. Schakel de appfuncties pas in nadat acceptatie is geregistreerd. De implementatie in de huidige app bewaart de acceptatiestatus lokaal in de browser; er wordt geen account aangemaakt.

```html
<label for="accept-terms">
  <input id="accept-terms" name="accept-terms" type="checkbox" required>
  Ik heb de <a href="./GEBRUIKSVOORWAARDEN.md">gebruiksvoorwaarden</a> gelezen en accepteer deze. Ik heb ook de <a href="./PRIVACYVERKLARING.md">privacyverklaring</a> gelezen.
</label>

<button id="start-app" type="button" disabled>Verder</button>

<script>
  const accept = document.getElementById('accept-terms');
  const start = document.getElementById('start-app');
  accept.addEventListener('change', () => { start.disabled = !accept.checked; });
  start.addEventListener('click', () => {
    if (!accept.checked) return;
    // Toon of activeer hier de app.
  });
</script>
```

Houd acceptatie van voorwaarden gescheiden van eventuele toestemming voor optionele verwerkingen, zoals analytics of marketing. Gebruik deze checkbox niet als vervanging voor toestemming als de wet voor een verwerking afzonderlijke toestemming vereist. Bepaal zelf hoe je acceptatie registreert; verzamel daarvoor niet meer gegevens dan nodig.

---
Dit is een sjabloon en geen formeel juridisch advies. Laat een jurist meekijken bij commercieel gebruik.
