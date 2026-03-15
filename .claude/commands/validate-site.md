Validate that the NorCal Trackdays site is live and functioning correctly.

## Steps

1. Use `curl -s -o /tmp/norcal-site.html -w "%{http_code}" https://davidyilee.github.io/norcal-trackdays/` to fetch the site and check the HTTP status code. Confirm it returns 200.
2. Read `/tmp/norcal-site.html` and verify it contains expected content: the three tracks (Laguna Seca, Sonoma Raceway, Thunderhill), filter controls, and the event table.
3. Check that event data is present in the HTML (look for event entries in the JavaScript `events` array).
4. Report the result: whether the site is **UP** or **DOWN**, and flag any issues found (missing content, broken structure, etc.).
