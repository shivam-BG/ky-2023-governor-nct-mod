# 2023 Kentucky Governor - New Campaign Trail Mod

Playable New Campaign Trail custom mod for the 2023 Kentucky gubernatorial election:

- Andy Beshear / Jacqueline Coleman
- Daniel Cameron / Robby Mills

The mod includes 25 questions, candidate-specific answer sets, Kentucky county scoring, issue maps, endings, and 2023 soundtrack metadata/search cues.

## Latest Fix

This version fixes the two common loader issues:

- Candidate/election images now use inline SVG data images, so the selection screens should not show broken image boxes.
- The `Latest Polls/Electoral Map` button now opens a Kentucky county-map panel with issue-map tabs instead of the stock national 2016 US map.
- Code 1 includes a fallback that fetches this repo's hosted Code 2 if NCT leaves you on the base 2016 Clinton/Booker question.

## How To Play

1. Open [The New Campaign Trail](https://www.newcampaigntrail.com/campaign-trail/index.html).
2. Click `Mod Loader`.
3. Choose `Other`, then open `Details`.
4. Paste `code1_2023_ky_governor.js` into Code Set 1.
5. Paste `code2_2023_ky_governor.js` into Code Set 2.
6. Click `Load`.
7. Close the loader and click `Click here to begin!`.
8. Pick Beshear/Coleman or Cameron/Mills.

## Files

- `code1_2023_ky_governor.js` - election setup, candidates, running mates, theme, credits, soundtrack metadata.
- `code2_2023_ky_governor.js` - 25 questions, answers, feedback, scoring, county baselines, endings, map hooks.
- `maps/*.svg` - Kentucky county issue maps.
- `ky2023_county_issue_scores.csv` - county issue score table.
- `ky2023_county_issue_scores.json` - same county issue data in JSON.
- `ky2023_preview.html` - local preview page for the SVG maps.

## Loader Compatibility

This mod uses NCT's stock election slot `20` internally so the custom loader can preload a valid base scenario before Code 2 runs. Visible scenario text, candidates, questions, answers, scoring, and results are all Kentucky 2023 content.

Internal IDs:

- Beshear/Coleman: `201/209`
- Cameron/Mills: `200/204`

If you still see the 2016 Clinton/Booker question, hard-refresh NCT, reopen the Mod Loader, and paste the newest Code 1 and Code 2 from this repo. The fallback should repair that screen automatically once the updated Code 1 is loaded.

## Maps

The included SVG maps cover:

- Beshear approval
- 2020 presidential margin
- Economy/jobs
- Social issues
- Disaster response
- Coal/energy
- Education/teachers

In-game map SVGs load from this repository's raw GitHub URLs. The map files are also included locally in `maps/`.

## Notes

- County baselines use public 2023 governor county results and 2020 presidential county results.
- Issue scores are modelled scenario scores for gameplay, not polling data.
- Soundtrack entries are metadata/search cues only. No copyrighted audio or lyrics are bundled.

## Sources

- [2023 Kentucky gubernatorial election county results](https://en.wikipedia.org/wiki/2023_Kentucky_gubernatorial_election)
- [2020 United States presidential election in Kentucky county results](https://en.wikipedia.org/wiki/2020_United_States_presidential_election_in_Kentucky)
- [U.S. county GeoJSON boundaries](https://github.com/plotly/datasets/blob/master/geojson-counties-fips.json)
- [AP Beshear path analysis](https://apnews.com/article/f942a360de22975335a1406f1fdd9ad4)
