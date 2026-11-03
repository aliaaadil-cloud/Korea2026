# Seoul Family Trip – 16–21 November 2026

A one-page, phone-friendly itinerary tracker built from itinerary v4.

## What it does
- **Itinerary tab** – Day 1–6 timeline. Each stop is tagged Place, Food, Transport or Stay.
- **Map buttons on every stop** – Naver Map, KakaoMap and Google Maps. Transport legs also have a Google transit directions button.
- **Tick stops as done** – progress is saved on your phone in that browser.
- **"NOW" highlight** – during the trip, the page opens on today's date in Seoul time and highlights the current stop.
- **Filter and search** – show only Places, Food, Shopping or Transport, or search across all days (for example "hanbok" or "Line 5").
- **Halal food tab** – every lunch and dinner, with halal status, hours and map links.
- **Info & to-do tab** – bookings checklist, accommodation, sunset and opening-time notes, and emergency numbers.
- **Costs tab** – an estimated price for every place, meal, ticket and ride, day by day, for each person and for the whole family, in ₩ and RM. You can change the exchange rate and the number of people. It also includes a suggested shopping allowance for each shopping stop, a simple tracker for what you actually spend (saved on that phone), and the original budget table.
- **Daiso** – Daiso Dongdaemun (Day 2, 8:30 PM), a quieter branch than the one in Myeongdong.

## Put it on GitHub Pages (about 5 minutes)
1. Sign in at github.com and click **New repository**. Give it a name such as `seoul-trip` and choose **Public**. Free GitHub Pages needs a public repo.
2. Click **Add file → Upload files**, drag in `index.html` (and this README if you like), then click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, then click **Save**.
4. Wait 1–2 minutes and refresh the page. It shows your link, for example `https://<your-username>.github.io/seoul-trip/`.
5. Open the link on each family member's phone and use **Add to Home Screen** so it opens like an app.

## Changing the itinerary
Open `index.html` and edit the `DAYS` list near the bottom, inside `<script>`. Each stop looks like this:

```js
{ t: "12:00 PM", type: "food", title: "Lunch · Ildossi Dakgalbi (Gwanghwamun)",
  desc: "Halal-certified Korean spicy stir-fried chicken.",
  ko: "일도씨닭갈비 광화문점", en: "Ildossi Dakgalbi Gwanghwamun", halal: "cert" }
```

- `type`: `place`, `food`, `shop`, `move` (transport) or `stay`
- Prices live in the `COSTS` list (₩ per person, keyed by day number starting at 0 and the stop title) and in `SHOPPING`.
- `ko` / `en`: the search names used for the map buttons. Korean names work best on Naver and Kakao.
- `from` / `to` (transport only): start and end points for Google transit directions.
- `halal`: `cert`, `friendly` or `check`
- `note` (optional) shows a highlighted note; add `warn: true` to make it yellow.

To publish an edit, upload the new `index.html` to the repo again. The site updates within a minute or two.

## Privacy note
A public GitHub Pages site can be opened by anyone who has the link. The page does not include travellers' names, passport details or the exact Airbnb address, only "Omok-ro, Yangcheon-gu". Keep it that way.
