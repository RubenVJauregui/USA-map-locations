# WISE Facility Map Dashboard

This is a static, editable sandbox project for the supplied facility map dashboard. The original standalone HTML is preserved as `index.html`; its facility data, interactions, links, external images, and Google Maps embeds remain self-contained in that file.

## Edit

Open `index.html` in your editor. The page's HTML, CSS, data, and JavaScript are all contained in that file.

## Run

Install dependencies once:

```sh
npm install
```

Start the static server:

```sh
npm start
```

Then open `http://localhost:4173`. The server listens on `0.0.0.0:4173` so it can be exposed by a sandbox preview.

## Listing-based facility details

The following previously incomplete right-side panels were enriched from the exact-address listing URL stored in the matching workbook tab:

- 146-El Paso: https://www.showcase.com/12104-emerald-pass-dr-el-paso-tx-79928/39995180/
- Airport: https://www.cimls.com/lease-listing/485982/industrial-3950-e-airport-drive-Ontario-CA
- Citypark: https://www.cimls.com/lease-listing/490098/industrial-8833-citypark-loop-houston-tx-77013-Houston-TX
- Cotton: https://www.cimls.com/lease-listing/480780/industrial-6801-n-cotton-lane-Waddell-AZ
- Ignition/Jacksonville: https://www.cimls.com/lease-listing/486037/industrial-2619-ignition-dr-Jacksonville-FL
- Plano: https://www.cimls.com/lease-listing/490097/industrial-910-10th-st-plano-tx-75074-Plano-TX
- Somerset: https://www.cimls.com/lease-listing/489423/storage-101-cottontail-ln-Somerset-NJ
- University Park: https://www.cityfeet.com/cont/listing/701-central-ave-university-park-il-60484/cs39223359

Downloaded source-listing images are stored in `assets/listings/`. Citypark and Plano intentionally use neutral "Listing image" labels because their source images are identical.

The 15 El Paso gallery images in `assets/listings/el-paso/` were cropped without upscaling from the user-supplied 1486 x 574 contact sheet, `Screenshot 2026-09-24 093600.png`. They are labeled neutrally as user-provided listing images and are not attributed to the Showcase CDN.

## User-supplied facility views

The following local assets in `assets/listings/facility-views/` were optimized without resizing from user-supplied PNG files and are scoped only to the named Facility Views slots:

- `Airport street.png` -> Airport Street picture
- `university  park ariel.png` -> University Park Satellite aerial view
- `University Park street.png` -> University Park Street picture
- `quality street.png` -> Quality Street picture
- `city park ariel.png` -> Citypark Satellite aerial view
- `City park street.png` -> Citypark Street picture
- `Plano street.png` -> Plano Street picture
- `roanoke ariel.png` -> Roanoke Satellite aerial view
- `willow arial.png` -> Willow Satellite aerial view
- `Willow street.png` -> Willow Street picture
- `Moreno valley street.png` -> Moreno Valley Street picture
- `Tacoma arial.png` -> Tacoma Satellite aerial view

`Screenshot 2026-09-24 101820.png` is byte-identical to `Airport street.png` and was intentionally deduplicated.

The seven top Features rows from the user-supplied `roanoke features.png` screenshot were transcribed into Roanoke's Features section. Its Available Spaces and Property Overview narrative were intentionally excluded; the existing unrelated Roanoke catalog facts remain present after the seven supplied rows.

Moreno Valley's listing enrichment remains blocked because its workbook URL returned an access-denied page; only the user-supplied street picture above was added. Quality's listing enrichment remains blocked because its workbook `C1` link is blank; only its user-supplied street picture was added. Remote Showcase and CityFeet images were not included because they did not load reliably. Listing availability and terms are presented as historical source statements and must be reverified before operational use.
