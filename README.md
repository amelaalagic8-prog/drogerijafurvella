# Drogerija Furvella

Statična web trgovina za kućne ljubimce, spremna za GitHub Pages.

## Sadržaj

- `index.html`: cijeli sajt (intro, trgovina, vodič, o nama, podnožje)
- `img/`: slike proizvoda i naslovna slika
- `favicon.svg`: ikona u kartici preglednika
- `.nojekyll`: GitHub Pages ne dira fajlove

## Objava na GitHub Pages

1. Na github.com napravi novi repozitorij (npr. `furvella`), javni.
2. Klikni **Add file → Upload files** i prevuci SVE iz ove mape (i mapu `img`).
   Ako se `.nojekyll` ne vidi, nije problem.
3. Klikni **Commit changes**.
4. Idi na **Settings → Pages**. Pod *Source* izaberi **Deploy from a branch**,
   grana **main**, mapa **/ (root)**, pa **Save**.
5. Za minut-dva sajt je na `https://TVOJE-IME.github.io/furvella/`.

## Narudžbe

GitHub Pages nema server, pa narudžbe rade na jedan od dva načina.
Podešava se na vrhu skripte u `index.html`:

```js
const ORDER_EMAIL="info@furvella.shop";
const FORM_ENDPOINT="";
```

- **Samo e-mail (zadano):** upiši svoju adresu u `ORDER_EMAIL`. Kad kupac
  pošalje narudžbu, otvori mu se e-mail program s popunjenom narudžbom
  (ime, prezime, e-mail, telefon, adresa, proizvodi, ukupno) i on je pošalje.
- **Formspree (preporučeno):** besplatno se registruj na formspree.io, napravi
  formu i kopiraj njenu adresu u `FORM_ENDPOINT`, npr.
  `const FORM_ENDPOINT="https://formspree.io/f/abcdwxyz";`
  Narudžbe tada stižu direktno u tvoj inbox, bez otvaranja e-mail programa.

## Šta nije u ovoj verziji

Recenzije kupaca i tvoja tabela "Podaci klijenata" trebaju bazu podataka,
pa ih u ovoj statičnoj verziji nema. Na claude.ai verziji i dalje rade.
