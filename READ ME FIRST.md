# TTT Helper: who gets which link

| Who | Gets | Link |
|---|---|---|
| **Riders** | the rider page | https://yfhg26.github.io/Team_Time_Trial/ |
| **DS (Android / no Python)** | the DS page | https://yfhg26.github.io/Team_Time_Trial/ds-k7m2q9.html |

Keep the DS link private: do not put it in the GitHub README or send it to riders.
The DS on a PC/Mac or iPhone can instead use a file from folder B or C (see below).

**Race day:** the DS opens their page, loads the plan, taps the broadcast icon, starts a live session and sends the
code. Riders open their link, type the code, tap Join, then tap their own name.

On GitHub only these files go in the repository, with exactly these names (lower case):
`index.html` (rider) and `ds-k7m2q9.html` (DS). `rider-buz7g9wnf3.html` is an optional spare rider link:
https://yfhg26.github.io/Team_Time_Trial/rider-buz7g9wnf3.html
Never put B1 on GitHub: it holds the key.

---

## Full file guide

Three roles, labelled by the first letter of each folder.

## A. RIDER: follow only, no planning (stripped view)
Joins a DS's live session with a code. No plan builder, no import, no hosting, no settings. No key.

| Folder | File | How a rider uses it |
|---|---|---|
| A2_WEB_PAGE_for_GitHub_index | `index.html` | Upload to GitHub. Riders open the link. Nothing to install. |
| A3_WEB_PAGE_for_GitHub_random_link | `rider-buz7g9wnf3.html` | The same page under a random name, for a less guessable link. |
| A1_PYTHON_file | `APV_TTT_v4_RIDER_follow_only.py` | Python on PC/Mac or Pythonista on iPhone. Same stripped view. Rarely needed. |

## B. DS WITH the ZwiftGopher API (builds plans in the app)
Needs Python (PC or Mac) or Pythonista (iPhone). Runs the race and shares the live code.

| Folder | File | Key |
|---|---|---|
| B1_PYTHON_key_included_PRIVATE | `APV_TTT_v4_DS_with_API_key_included_PRIVATE.py` | Team key built in. Plan builder works at once. **Keep private.** |
| B2_PYTHON_enter_your_own_key | `APV_TTT_v4_DS_with_API_enter_own_key.py` | No key inside. The DS pastes their own key into the app once. |

## C. DS WITHOUT the API (loads a ZwiftGopher JSON file instead)
Same race screen and live sharing, but no plan builder. Make the plan on the ZwiftGopher site, export JSON, import it.

| Folder | File | For |
|---|---|---|
| C1_WEB_PAGE_for_GitHub_Android | `ds-k7m2q9.html` | A DS who cannot run Python (Android). Open the link in Chrome. Share the link with the DS only. |
| C2_PC_Mac_double_click_file | `APV_TTT_v4_DS_no_API_JSON_only_PC_Mac.html` | A DS on a PC or Mac. Double-click it. Nothing to install. |

## A race
1. The DS opens a B or C file, loads or builds the plan, taps the broadcast icon and starts a live session.
2. The DS sends the session code to the riders.
3. Riders open the rider link (A2 or A3), type the code, tap Join, then tap their own name. That turns their sound on and lets their phone warn them (red) before their pull and show green when they are on.

## Links (GitHub Pages, repository `yfhg26/Team_Time_Trial`)
- Rider (A2): https://yfhg26.github.io/Team_Time_Trial/
- Rider, random link (A3): https://yfhg26.github.io/Team_Time_Trial/rider-buz7g9wnf3.html
- DS web page (C1, DS only): https://yfhg26.github.io/Team_Time_Trial/ds-k7m2q9.html

Files that go on GitHub must keep their exact names (`index.html`, `rider-buz7g9wnf3.html`, `ds-k7m2q9.html`), all lower case.
Never put B1 on GitHub: it holds the key.

## Still to check with real devices
- An iPhone rider hearing the first countdown (the name-picker tap should now unlock sound; not testable here).
- The DS web page (C1) on a real Android phone.
- The new rider Python file (A1) on a real device. I tested it in a browser against a stand-in relay.
- A short test session with a DS and a rider on separate devices before race day.

© 2026 TTT Helper. All rights reserved.

## What changed from the previous labelled set (v9)
- All files: every screen restyled to the canvas look (dark, green = on the front, red dashed = next, white main buttons).
- Rider files (A1, A2, A3): "Who are you?" step, one-tap sound, and the red YOU'RE NEXT / green YOU'RE ON band.
- DS files (B1, B2, C1, C2): look only. The name picker is inside but switched off.
- Not built: Undo, confirmations on Skip/Drop, "Who's missing?" and greyed-out taken names (see the report).
