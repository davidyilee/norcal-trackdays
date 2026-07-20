# Plan: Event data refresh — July 19, 2026

## Goal
Bring the `events` array in `index.html` up to date as of 2026-07-19. Data was last
verified March 2026. Focus on the remainder of the 2026 season (late July–December),
plus corrections to existing entries (prices that were TBD, cancelled/moved events).

## Approach
1. Parallel research agents, one per source cluster:
   - Moto orgs: Fun Track Dayz, Pacific Track Time, Volant Vivere
   - Moto orgs: Carters@theTrack, Keigwins@theTrack
   - Schools: CA Superbike School, Yamaha ChampSchool
   - Car/HPDE: Hooked On Driving, SpeedSF, NASA NorCal
   - Car/HPDE misc: Sonoma Raceway open track days, TrackMasters, LightSpeed, Serge, GGLC
   - Spectator/big events: WeatherTech Raceway season events, MotoAmerica
2. Merge verified results into the `events` array; keep past 2026 events (it is a
   season-wide schedule), update prices, add new events, drop confirmed cancellations.
3. Update the sources comment block ("verified July 2026").
4. Verify the page renders locally, then commit.

## Progress log
- 2026-07-19: Plan written; research agents launched.
- 2026-07-19: All six research reports returned; Z2 Track Days verified directly
  (new organizer, 4 events added). Merged into `index.html`: 84 → 114 events.
  - Added: LightSpeed fall calendar (6), Serge invite-only dates (6 upcoming +
    relabeled Apr 4–5), GGLC (3), Sonoma Open Track Days Jul 28 + Aug 27, SpeedSF
    fall dates (6), Z2 (4), HOD Sep 10 Thunderhill Thursday, Laguna spectator
    events (Pre-Reunion, GRIDLIFE, Racing America/Trans Am).
  - Corrected: Carters Sep 14–15 "AFM Race Weekend + Novice School" → Sep 14
    regular track day (NRS day is Sep 25); Carters Sep 21 Laguna is a track day,
    not a school; NASA 12 Hours of Thunderhill is Sep 18–19 @ $2,195/team;
    TrackMasters Mar 6–7 → Mar 6; PTT Sep 12–13 East $279/day; FTD Laguna May
    days were $669 not $600; VV Sep 24 → waitlist-only; dead URLs re-pointed
    (VV removed past-event pages, FTD apr-20 page gone); NASA rows now link
    to specific event pages; HOD fall events renamed/priced per motorsportreg.
  - Removed: Keigwins placeholder note (zero 2026 events; Carters is the
    successor operation — noted in sources comment).
  - Validated with Node: all dates/tracks/types/URLs well-formed; page renders.
- 2026-07-19: Committed and pushed to Main for GitHub Pages deploy.
