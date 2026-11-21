# The Thin Hours: Carmo vertical slice

Playable prototype: web (any browser) and Android (Capacitor).

## Play in a browser
Open www/index.html through any static server, for example `npx serve www`.

Touch / gamepad: left stick or D-pad moves, A jump, B dash (brief invulnerability), X strike, tap Y to Survey.
Keyboard: A/D move, Space jump, L dash, J strike, hold K to Survey.
Touch: on-screen buttons.

## Get the APK from GitHub
1. Create a new GitHub repo and push this folder to the `main` branch.
2. Open the Actions tab, run "Build Android APK" (it also runs on every push).
3. When it finishes, download the `thin-hours-debug-apk` artifact from the run page.
4. Unzip it, copy `app-debug.apk` to your phone and install it (allow installs from this source).

The APK is a debug build signed with the debug key. Good for testing and sideloading, not for the Play Store.

## Gameplay notes
- Walk up to a lantern-and-trunk cache and press A: rest (full health, becomes your respawn point) and swap the carried weapon.
- Wardens have hit zones: head (double damage, needs a jump strike), chest (seam glows under Survey), arms (interrupt a raised slam) and legs (slow it). Survey (tap Y) shows the zones.
- The first Warden is dormant and gentle; the route ramps up from there.

## Difficulty and testing notes
- Wardens hold their stance during a slam (spamming strike gets you hit), stagger builds slowly and resets, and a perfect dodge opens a counter-strike window.
- Each kill restores 1 vitality. The boss has three phase breaks that restore 2 each.
- Assist: after repeated defeats in the same stretch of route, Wardens wind up more slowly and take slightly more damage. It resets when you light the next anchor.
- Balance was checked with scripted players (expert, average, novice, masher) over the full route, not with human playtesters.
