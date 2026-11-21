# NBA Courtside | The Modern Era

By Julian Devonish. Interactive Tableau portfolio using observed NBA statistics, not simulated data.

Published: https://public.tableau.com/app/profile/jul.dev/viz/NBACourtside-TheModernEra/01Courtside

## Explore

1. Courtside: league scoring, shot selection, pace, completed games, player leaders and team win percentages. Its Starting Five portraits update with season, competition and the leaderboard metric, using the same eligibility and rank filters as the chart.
2. Matchup Lab: two selected players, scoring, rebounds, assists, true shooting and their scoring history across the era.
3. Team Identity: offense versus defense, net rating, three-point volume versus accuracy and team scoring.
4. Evolution: 13-season trends in league scoring, three-point share, pace and accuracy.
5. Start Here: data scope, counting units, calculations, controls and limitations.

## Data and provenance

NBA.com Stats observations accessed through Larry's public nba_data mirror: https://github.com/llimllib/nba_data and https://basketball-data.billmill.org/nba/ . See sources.json for the 52 source files, download timestamps and SHA-256 hashes. The extraction covers 2014–15 through 2026–27, regular season and playoffs separately, through 20 November 2026. The current season is partial. This is a static published snapshot, not a live feed.

The prepared extract contains 9,546 player-season/competition records, 582 team-season/competition records and 25 league aggregates. Each view filters to exactly one record type to prevent double counting. Team figures derive from 31,332 paired team-game observations representing 15,666 games. Preseason, All-Star, play-in and NBA Cup final IDs are excluded. Player season totals are retained for traded players; team labels show their final recorded team for the season.

## Calculations and checks

- Player rates divide totals by the player's appearances. Team and league rates divide by team appearances. League game count divides team appearances by two.
- True shooting: PTS / (2 × (FGA + 0.44 × FTA)). Three-point share: 3PA/FGA. Three-point accuracy: 3PM/3PA.
- Offense and defense: points scored/allowed per 100 source possessions. Net rating is offense minus defense. Pace averages the source game pace across team appearances.
- Player point totals reconcile exactly to team totals for all 25 season/competition combinations. Scoring arithmetic, paired game margins, win flags and duplicate keys were checked.
- The 2015–16 Curry check reproduces 402 three-pointers in 79 appearances, or 5.1 per game when rounded.
- Exploratory leaderboard eligibility requires at least five appearances and 15 minutes per game; this is not official NBA statistical qualification. Matchup comparisons apply no such threshold.
- Team bar charts show the top 15 by win percentage; alphabetical team labels break ties at the cutoff. Scatter plots include every team in the selected scope.

Missing player-season observations are blank rather than zero. 2026–27 playoffs have no observations. Rates do not adjust for role, minutes, opponent quality, roster changes or rules. Descriptive comparisons do not establish causes.

## Images

Player portraits originate from NBA.com's public CDN. See image-credits.json and dynamic-portrait-credits.json. The opening Starting Five embeds 112 portrait assets covering every player who enters a top five in the snapshot. Each slot filters to rank 1–5 in the selected season, competition and metric. Ties use unrounded rates and alphabetical names. Other pages retain decorative era portraits; selected player names identify matchup statistics. Latest portraits are not historical jersey representations. Unofficial fan analytics; no NBA endorsement.

## Reproduce

Run fetch_data.py, prepare_data.py, create_assets.py, create_dynamic_portraits.py and build_workbook.py in that order with Python, DuckDB, Pillow and the Tableau Hyper API. The build script expects the Hyper API runtime under work/tableau_runtime relative to the project workspace; adjust that import path for another environment. The workbook embeds its extract, source CSV and graphics. validation.json records dataset checks; calculated-fields.json documents Tableau formulas. The final packaged workbook is NBA Courtside - The Modern Era.twbx.
