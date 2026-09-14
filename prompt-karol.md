# Prompt dla agenta Karola — budowa strony Zespołu „Kundzia"

Zbuduj jednostronicową stronę internetową (landing page) dla zespołu tańca ludowego
„Kundzia" z Chełmna. Poniżej pełna specyfikacja.

## Technologia i ograniczenia
- Jeden plik `index.html` — cała strona (HTML + CSS + JS w środku, bez frameworków,
  bez build-stepu). Grafiki wstawiaj jako pliki obok lub data:URI base64.
- Strona statyczna, hostowana na Cloudflare Pages/Workers (git → auto-deploy).
- Język polski. Na początku pliku KONIECZNIE: `<!DOCTYPE html>` i `<meta charset="utf-8">`
  (inaczej polskie znaki ą/ę/ł/ó się psują).
- W pełni responsywna (poprawnie od ~360px do desktopu), z obsługą trybu jasnego
  i ciemnego (`prefers-color-scheme`).
- Dodaj plik `_headers` z regułą `Cache-Control: no-cache` dla `/` i `/index.html`,
  żeby wymuszać świeżą wersję.

## Marka
- Nazwa: Zespół Tańca Ludowego „Kundzia", Chełmno, woj. kujawsko-pomorskie.
- Logo: plik `logo-kundzia.png` (tancerka + napis KUNDZIA) — w nagłówku po lewej.
- Facebook: https://www.facebook.com/ztlkundzia/ ; Instagram: (do uzupełnienia).

## Kolory i typografia
- Czcionki z Google Fonts: „Zilla Slab" (nagłówki) + „Figtree" (tekst).
- Motyw jasny: tło białe (#FFFFFF), sekcje naprzemienne bardzo jasnoszare (#F4F5F7),
  tekst ciemny (#231B15), akcent czerwony (#B23127 / ciemniejszy #8C2019),
  obramowania jasnoszare (#E6E7EA). Stopka ciemnogranatowa (#1E2A48) z jasnym tekstem.
- Motyw ciemny: analogicznie ciemne tła, jasny tekst.
- Zaokrąglenia ~14px, delikatne cienie, przyciski czerwone z efektem hover.

## Nagłówek (górny pasek)
- MUSI być przyklejony na stałe do góry: `position:fixed; top:0; left:0; right:0`
  (nie `sticky`!). Dodaj `body { padding-top: <wysokość paska> }`, żeby treść się nie chowała.
- Zawartość: logo po lewej (wys. ~66px, przesunięte lekko w prawo), menu na środku/prawo,
  po prawej czerwony przycisk „Dołącz do nas".
- Menu (kotwice do sekcji): Aktualności, Wydarzenia, Festiwal, O nas, Sukcesy,
  Galeria, Dokumenty, Kontakt. Dodaj `scroll-margin-top`, by kotwice nie chowały się pod paskiem.
- Pasek solidnie biały (nieprzezroczysty), z subtelnym cieniem.

## Sekcje (kolejność od góry)
1. **HERO**: duży baner-zdjęcie zespołu, pod nim nagłówek pionowo do lewej:
   H1 „Zespół Tańca Ludowego Kundzia" + podpis „Barwny folklor z Chełmna —
   na scenach całej Europy." Zostaw wyraźny odstęp pod hero.
2. **WYDARZENIA** (dwie kolumny):
   - Lewa: lista wydarzeń — każde jako kafelek z czerwonym „kafelkiem daty"
     (dzień + skrót miesiąca), tytułem, meta (miejsce · godzina) i krótkim opisem.
   - Prawa (węższa kolumna): zdjęcie zespołu + boks „O zespole w skrócie"
     z krótkim opisem i przyciskami Facebook oraz Instagram (jeden pod drugim).
3. **AKTUALNOŚCI I WYJAZDY**: na całą szerokość, kafelki „news" (zdjęcie + kraj/rok +
   tytuł + opis). Kafelki KLIKALNE — po kliknięciu otwierają modal (okno) ze zdjęciem
   i pełnym opisem; zamykanie krzyżykiem, klawiszem Esc i kliknięciem w tło;
   obsługa klawiatury (Tab/Enter). Na kafelku podpowiedź „Czytaj więcej →".
4. **O NAS**, 5. **SUKCESY**, 6. **GALERIA** — sekcje treściowe w tym samym stylu.
7. **FESTIWAL**: osobna sekcja o festiwalu organizowanym przez zespół, z opisem,
   akapitem „Chcemy wrócić!" i siatką miejsc na zdjęcia.
8. **DOKUMENTY**: sekcja „do pobrania" z przyciskami-plikami (PDF): Deklaracja członkowska,
   Standardy ochrony małoletnich, Klauzula RODO, Statut. Przyciski jako linki do plików PDF.
9. **KONTAKT**: dane kontaktowe + link do Facebooka.
10. **STOPKA**: ciemnogranatowa, z nazwą, lokalizacją, menu i notką o prawach autorskich
    oraz automatycznie wstawianym rokiem (JS).

## Zachowania / detale
- Sekcje naprzemiennie na białym i bardzo jasnoszarym tle (rytm wizualny).
- Efekty hover na kafelkach i przyciskach (lekkie uniesienie, cień).
- Cały interfejs po polsku, estetyka: folklor, ciepło, czytelność.

## Treści przykładowe
Tam gdzie brak realnych danych (wydarzenia, opis festiwalu, pliki PDF), wstaw estetyczne
treści przykładowe (placeholdery), które łatwo podmienić — i oznacz je do uzupełnienia.
