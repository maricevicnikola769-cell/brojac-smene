# Brojač smene

Jednostavna aplikacija za brojanje tokom smene:

- Stranke domaće
- Stranke strane
- Pregledana putnička vozila
- Pregledana teretna vozila
- Posete službenih vozila
- Posete u okviru službenih poseta

U dnevnoj smeni se posle **17h**, a u noćnoj posle **5h** broji posebno. Dugme **Završi smenu** briše sve brojeve (uz opciju da se izveštaj prvo kopira).

Brojevi se čuvaju samo na uređaju na kom se unose. Aplikacija radi i bez interneta i može da se doda na početni ekran telefona.

## Postavljanje na GitHub Pages

1. Napravite novi repozitorijum na GitHub-u (npr. `brojac-smene`).
2. Otpakujte arhivu i postavite **sve fajlove i folder `icons`** u koren repozitorijuma
   (na GitHub-u: *Add file → Upload files*, prevucite sve i kliknite *Commit changes*).
3. Idite na *Settings → Pages*, pod *Build and deployment* izaberite
   *Source: Deploy from a branch*, grana `main`, folder `/ (root)`, pa *Save*.
4. Posle minut-dva aplikacija je na adresi
   `https://VAŠE-KORISNIČKO-IME.github.io/brojac-smene/`

## Dodavanje na početni ekran

- **Android (Chrome):** otvorite adresu → meni ⋮ → *Dodaj na početni ekran* / *Instaliraj aplikaciju*.
- **iPhone (Safari):** otvorite adresu → dugme *Deli* → *Dodaj na početni ekran*.

## Fajlovi

| Fajl | Namena |
|---|---|
| `index.html` | cela aplikacija |
| `manifest.webmanifest` | naziv, boje i ikonice za instalaciju |
| `sw.js` | rad bez interneta |
| `icons/` | ikonice (SVG i PNG) |
| `.nojekyll` | GitHub Pages servira fajlove bez obrade |

## Izmena aplikacije

Posle izmene `index.html` promenite i `CACHE = "brojac-v1"` u `sw.js` (npr. u `brojac-v2`) da bi telefoni sigurno preuzeli novu verziju.
