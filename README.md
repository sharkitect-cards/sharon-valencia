# Dra. Sharon Valencia Álvarez — digital card

Live: https://cards.sharkitectdigital.com/sharon-valencia/
Contact file (what the QR and the NFC chip point at): `/sharon-valencia/contact.vcf`

Built 2026-09-10. First Sharkitect card outside the United States.

## Whose words these are

**Every line of content on this card came from the client or from her own published
profiles. Sharkitect did not author any claim, tagline, or description here.**

| On the card | Source |
|---|---|
| Dra. Sharon Valencia Álvarez | Her legal name is *Jessrel Sharon Valencia Álvarez* (Hospital Galenia's own listing). She goes by Sharon. The displayed form was approved by the client 2026-09-10. |
| Cardióloga y Ecocardiografista | **Her own wording**, taken verbatim from her Instagram bio (`@cardio_valencia`, read 2026-09-10). Preferred over the hospital's phrasing because it is how she describes herself. |
| Cédula Profesional 12505405 | Her Doctoralia profile. |
| Centro Cardiológico y Pulmonar · Hospital Galenia | The hospital's own cardiology page. |
| Torre B · Consultorio 412 · Av. Tulum SM 12, Cancún | Her WhatsApp Business listing, corroborated by the hospital page. |
| Phone, email, Doctoralia, Instagram, Facebook | Supplied by the client. |

Nothing on this card is private. Her phone, email, office, specialty and licence number
are already published on her own Doctoralia profile and on the hospital's website.

## Build decisions

- **No business name on the card face** (client direction, 2026-09-10). Her name only. The
  Beat & Breathe logo still serves as the brand mark — centred in the QR and used as the
  home-screen icon — but no company text line appears.
- **Spanish first, English toggle.** She treats patients in both languages and Cancún is an
  international city. The choice is remembered per-device.
- **Brand colours sampled from her logo file**, never guessed: teal `#009C90`, blue
  `#0054B4`, gold `#E99103`.
- **Doctoralia occupies the website row.** She has no website of her own, and Doctoralia is
  where she wants patients booking. `hospitalgalenia.com` is her employer's site and is
  deliberately absent.
- **Divider glyph is a heart**, echoing the mark in her own logo (design standard §5).

## Verification run before publishing

- QR decodes at 100 %, 50 %, 25 % and 15 % scale — machine-checked, not eyeballed.
- `contact.vcf`: 55 KB, photo embedded on a single unfolded line, CRLF endings, **0 bare
  LF** (a bare LF makes some handsets silently refuse to save the contact).
- Page passes `tools/card-builds/verify_card_standard.py` — exactly one `save-btn` calling
  `toggleQR()`, no `saveContact()`, no direct `.vcf` anchor, no second button.
- Both languages and the QR overlay rendered and clicked through in a real browser.

## Known item for the client

Her **Doctoralia profile lists her practice name incorrectly as "Beat and Health Integral."**
Her actual practice name is **Beat & Breathe — Salud Integral**. Worth her correcting, since
it is her own booking page.

## Not deployed

`headshot-master.png`, `logo.png`, `hero.png` and `build-assets.py` are build sources and are
deliberately kept out of this repo.
