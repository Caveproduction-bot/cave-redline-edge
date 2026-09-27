# Privacy — Cave Redline Edge

**Short version: nothing leaves your PC. There is no account, no telemetry and no
analytics. Neither the widget nor the bridge sends anything to the internet.**

## What the widget stores

The widget keeps its data in the browser storage iCUE provides for it, under the
`cave-redline-edge` name, on your own PC:

| Key | Contents |
| --- | --- |
| `tasks` | Your tasks: title, description, due date, duration, priority, and whether and when each was completed |
| `task-memory` | Titles, descriptions, durations and priorities of tasks you have saved before, for suggestions |
| `task-stats` | Your running count of completed tasks and the planned time credited when tasks are ticked off by hand |
| `stopwatch` | Whether the work timer is running, its start time, time worked so far and your goal |
| `break-timer` | Break end time and the number of breaks taken |
| `work-settings` | Break length, reminder settings, automatic logging, and the task the current session is for |
| `work-session-history` | Logged sessions: start and end times, time worked, paused time, breaks, goal and linked task or project |
| `preferences` | Clock format, Movie Mode brightness, whether completed tasks show in Up Next, and your last chosen sound output and media app |
| `icue-style` | The last colours iCUE sent, so the dashboard opens in the right colours |

None of it is ever transmitted. **Options → Reset all data** deletes all of it, and
removing the widget from iCUE removes it too.

## What the widget reads

Track and artist come from iCUE's official Media Data Provider. Everything else comes
from the bridge, below. The widget does not store media information.

## What the bridge does

The Cave Redline Edge Bridge is a Windows companion program. It:

- listens only on `http://127.0.0.1:47152`, your own PC, so nothing on your network or
  the internet can reach it, and refuses requests from websites;
- reads your sound devices' names, volume and mute state, and changes them when you tap;
- reads what Windows media sessions are playing (title, artist, app, artwork and
  position) and sends play, pause, skip and seek commands when you tap;
- reads CPU, GPU, RAM and network usage;
- reads how many Windows notifications you have. It reads the count only, never their
  content;
- reads the XENEON EDGE Screen Setup keyboard shortcuts from iCUE's settings file,
  without changing them, and presses them only when you tap the display-mode button or
  swipe between pages;
- presses Windows + D when you tap Show desktop, opens iCUE when you tap Open iCUE,
  opens Windows' own Task Manager when you tap TASK MANAGER, and opens the Tom's Cave
  shop page in your web browser when you tap that button;
- locks your PC when you tap Lock, and asks Windows to shut down or restart when you
  press and hold Shut Down or Restart. It never forces this: Windows can still ask to
  close apps, and you can still cancel.

It keeps no history of your media, sound or readings. It writes three small diagnostics
files in `%LOCALAPPDATA%\CaveRedlineEdge\`, all on your own PC and never sent anywhere:

- `origins.log`: the kinds of programs that have contacted it (for example `file://`
  for iCUE), capped at 50 lines;
- `bridge-start.log`: when it started or why it stopped, capped at 20 lines;
- `power-audit.log`: the time of each Lock, Shut Down or Restart request and what Windows
  answered, capped at 1,000 lines, so you can always check what asked your PC to shut
  down and when.

The installer writes a log to your temporary folder if something goes wrong.

## Third parties

There are none: no SDKs, crash reporting, advertising or analytics.

## Your rights

No personal data is collected or transmitted, so there is nothing for Tom's Cave to
disclose, export or erase on request. Everything the Software knows is already on your
own PC and under your control.

## Contact

<https://github.com/Caveproduction-bot/cave-redline-edge/issues>
