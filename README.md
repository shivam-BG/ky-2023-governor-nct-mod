# 2023 Kentucky Governor - New Campaign Trail Mod

Playable New Campaign Trail custom mod for the 2023 Kentucky gubernatorial election:

- Andy Beshear / Jacqueline Coleman
- Daniel Cameron / Robby Mills

The mod includes 25 questions, candidate-specific answer sets, Kentucky county scoring, issue maps, endings, and 2023 soundtrack metadata/search cues.

Latest update:

- Added a drop-style `static_mod/` package modeled after released governor mods such as `2022AZGov`, `2022PAGov`, `2016NC`, and `1990 MI`.
- Added generated banner/background/icon assets and state-mod globals for `THE KENTUCKY TRAIL`, credits, historical result colors, and theme styling.
- Kept the custom-loader Code 1 + Code 2 flow working for normal NCT players.

Files:

- `code1_2023_ky_governor.js`: election metadata, candidates, running mates, theme, credits, and soundtrack metadata.
- `code2_2023_ky_governor.js`: 25 questions, answers for both Andy Beshear and Daniel Cameron, county baselines, answer effects, endings, and map hooks.
- `static_mod/`: drop-style `_init.html` and candidate-running-mate HTML files using the `2023KYGov` naming convention.
- `assets/*.svg`: generated banner, background, icon, and ticket-card art used by the drop-style theme.
- `maps/*.svg`: Kentucky county issue maps using real county boundaries.
- `ky2023_county_issue_scores.csv` / `.json`: source county scores used by the mod and maps.
- `ky2023_preview.html`: local preview page for the SVG maps.

How to use:

1. Open [The New Campaign Trail](https://www.newcampaigntrail.com/campaign-trail/index.html).
2. Click `Mod Loader`.
3. Choose `Other`, then open `Details`.
4. Paste `code1_2023_ky_governor.js` into Code Set 1.
5. Paste `code2_2023_ky_governor.js` into Code Set 2.
6. Click `Load`.
7. Close the loader and click `Click here to begin!`.
8. Choose Beshear/Coleman or Cameron/Mills.

Static drop package:

- The files in `static_mod/` are for a standard dropped-mod setup.
- Add `static_mod/mods_json_entry.json` to the site's mod list.
- Place `2023KYGov_init.html`, `2023KYGov_BeshearColeman.html`, and `2023KYGov_CameronMills.html` in the static mods folder.

Compatibility notes:

- The mod uses NCT's stock election slot `20` internally so the custom loader can preload a valid base questionset before Code 2 runs.
- The `static_mod/` folder mirrors the release pattern of governor drops like `2022AZGov`, `2022PAGov`, `2016NC`, and `1990 MI`: one init file plus candidate/running-mate Code 2 files.
- Beshear/Coleman use the stock-safe internal IDs `201/209`, and Cameron/Mills use `200/204`. The visible names, descriptions, questions, answers, scoring, and results are all Kentucky 2023 content.
- Code 2 filters the shared answer bank to the selected candidate, so the same Code 2 works for both Beshear and Cameron.
- Code 1 includes a fallback that fetches the GitHub-hosted Code 2 if the NCT loader leaves you on the stock 2016 base question.
- Candidate and election images are inline SVG data images, so the selection screens should not show broken image boxes.
- The `Latest Polls/Electoral Map` button is overridden with a Kentucky county-map panel and issue-map tabs. It does not use the stock national US map.

Notes:

- The county baselines use the public 2023 governor county results and 2020 presidential county results.
- The issue maps are modelled scenario scores, not polling data. They are designed to support gameplay: Beshear approval, 2020 presidential margin, economy/jobs, social issues, disaster response, coal/energy, and education/teachers.
- The in-game map panel loads the SVG issue maps from this GitHub repository's raw file URLs.
- The soundtrack contains popular 2023 song metadata/search cues only. No copyrighted audio or lyrics are bundled.

Sources:

- [2023 Kentucky gubernatorial county results](https://en.wikipedia.org/wiki/2023_Kentucky_gubernatorial_election)
- [2020 Kentucky presidential county results](https://en.wikipedia.org/wiki/2020_United_States_presidential_election_in_Kentucky)
- [U.S. county GeoJSON boundaries](https://github.com/plotly/datasets/blob/master/geojson-counties-fips.json)
- [AP Beshear path analysis](https://apnews.com/article/f942a360de22975335a1406f1fdd9ad4)
