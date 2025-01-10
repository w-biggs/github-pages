Minimum reproducible example for a weird Firefox bug.

**Expected behavior (Chrome and Safari)**: Page completes parsing, displays all numbers up to 172290, doesn't act as if page is still loading indefinitely.

**Observed behavior (Firefox)**: Page USUALLY stops parsing at some point, does not display all numbers, and acts as if page is stuck loading indefinitely. (Sometimes it will display all numbers successfully; doing a hard refresh / disabling cache makes the issue occur closer to 100% of the time.)

The issue doesn't occur if you change the script to load non-asynchronously or deferred.

I serve up the pages via `npx http-server . -p 8123` but you can serve it up however you prefer.

Bug filed on Bugzilla@Mozilla: https://bugzilla.mozilla.org/show_bug.cgi?id=1940828
