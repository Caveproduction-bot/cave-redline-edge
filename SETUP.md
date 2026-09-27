# Setting up Cave Redline Edge

Setup takes about two minutes. You need Windows, iCUE 5.47 or later, and a CORSAIR
XENEON EDGE.

## 1. Add the widget to your XENEON EDGE

1. Get **Cave Redline Edge** from Elgato Marketplace. iCUE installs it for you.
2. In iCUE, open your **XENEON EDGE** and go to the **Widgets** page.
3. Add **Cave Redline Edge** to a screen and give it the whole screen (the largest size).

The clock, tasks, the focus timer, colours and the CPU and GPU readings all work straight
away, with nothing else installed.

## 2. Choose your colours in iCUE

Cave Redline Edge is coloured from iCUE, in the same place as every other widget.

1. In iCUE, open your **XENEON EDGE**, go to **Widgets** and select **Cave Redline Edge**.
2. Under **Cave Redline Edge Personalization**, pick any **Accent Color**. The neon around
   the whole dashboard, the buttons, the progress bar and the graphs all follow it, and the
   rest of the dashboard is tuned to match.
3. The dashboard has two text colours. **Text Color 1** is the near-white of its
   headings, names and readings; **Text Color 2** is the cool blue of its labels,
   captions, due dates and links. Both are yours to change.
4. **Background Color** paints the whole dashboard, shell and all, in that colour: a
   strong colour gives a deep version of it, a pale one turns the dashboard over to a
   light version, and white, black and greys give the plain light or dark dashboard.
   The accent keeps the colour you picked either way.
5. **Background Transparency** fades the dashboard's background and panels, so the iCUE
   page (its Device Background colour or image) shows through, while text, numbers and
   buttons stay at full strength. It starts at 100%. On a black page background the
   change is subtle, because the dashboard is dark too.

These are the only colour settings Cave Redline Edge uses. iCUE's **Pages Personalization**
(Theme per Page, Widget Text Color, Widget Accent Color, Widget Background, Widget
Transparency) does not change it, on purpose: those settings are what dimmed the
dashboard on a new page and hid its own colour choices.

The dashboard changes as you pick. To go back to the original look, set the colours to
accent **#F51129**, text **#F3F6FA** and background **#070B10** (also listed in the
dashboard's **Options**). For other ready-made looks, use one of these accents:
blue **#5D9DD3**, green **#5FB58C**, yellow **#D6B45A**, orange **#D98F5A**.

Whatever you choose is checked for readability and nudged if a combination would be
hard to read, so the dashboard never ends up unreadable.

## 3. Where the CPU, GPU, RAM and network readings come from

These are found for you and need no setup. **Options → System readings** always names
the source behind each figure, so you can see what was found. If you would rather
choose, select **Cave Redline Edge** under **Widgets** in iCUE and use **System
Readings**:

- **CPU Source**, **GPU Source**, **RAM Source**: each starts on **Automatic**. Change
  one to **Manual** and pick from the sensors on your PC in the row below it.
- The sensor row is only read when its Source says **Manual**. iCUE keeps showing the
  last sensor you picked even after you go back to Automatic, which is why that row
  says "only used when Manual".
- **Network Source** starts on **Automatic**, which measures the connected Ethernet or
  Wi-Fi adapter that is carrying traffic. Set it to **Ethernet** or **Wi-Fi** to measure
  that kind of connection. The network reading's label shows which one it is using.
- Only the reading you change is affected; the rest stay automatic.
- If a sensor you picked is no longer there, that reading goes back to Automatic.
- **Network Source**: **Automatic** measures whichever connection is carrying traffic.
  Choose **Ethernet** or **Wi-Fi** to measure that one. The network box is labelled
  ETHERNET or WI-FI so you can see which is being measured.

iCUE has no sensor for system RAM on most PCs, and none at all for network speed, so
those two come from the bridge in the next step. A reading with no source shows **N/A**
and a short note saying why and where to fix it, and the status at the bottom right says
which one to set up.

## 4. Install the free Cave Redline Edge Bridge

The bridge is a small program that lets the dashboard reach Windows. It powers:

- volume, mute, microphone mute and switching sound output
- album artwork, the progress bar and switching between media apps
- the RAM and network readings
- the Windows notification count, and opening and closing the notification centre
- Show desktop, the display-mode button, swiping between pages, TASK MANAGER, and
  Open iCUE
- Lock, Shut Down and Restart

Without it, those parts of the dashboard say so. Tasks, the focus timer, the clock,
colours and the CPU and GPU readings do not need it.

1. Download **CaveRedlineEdgeBridge-Setup.exe** from
   <https://github.com/Caveproduction-bot/cave-redline-edge/releases/latest>.
2. Double-click it. If Windows shows "Windows protected your PC", click **More info**,
   then **Run anyway**. The installer is not code-signed, which is why Windows asks.
3. After a few seconds a message says the bridge is installed and running.

The bridge starts automatically whenever you sign in to Windows, and uses almost no
resources. You only need to install it once. Run a newer installer to update it.

## 5. Swiping between pages and the display-mode button

Cave Redline Edge uses the keyboard shortcuts **you** set in iCUE, so they match however
you already use your XENEON EDGE.

1. In iCUE, open your **XENEON EDGE** and go to **Screen Setup**.
2. Click **Add Keystroke** next to each of these and press a shortcut you don't use
   anywhere else:
   - **Switch Display Mode**: used by **DISPLAY MODE** in the top bar
   - **Previous Display Screen**: swipe right on the dashboard
   - **Next Display Screen**: swipe left on the dashboard

Shortcuts such as Ctrl + Alt + Shift + F10, F11 and F12 work well because nothing else
uses them. If a shortcut isn't set, the dashboard tells you when you try to use it.

## Using it

- **Tasks:** tap **ADD TASK**. Start typing a title and past tasks are suggested. Tap
  the date for a calendar. Pick a duration or type one, such as "45 min" or "2h".
- **Current focus:** tap ▶ on a task to make it your focus and start its timer. **BREAK
  TIME** starts a break, and **END TASK** saves the session and ticks the task off.
  Ticking the task off yourself ends and saves its session too. Tap **GOAL** to change
  the goal and break length.
- **One task at a time:** if a session is running and you start a different task, the
  dashboard asks you to end and log that one first. Tapping ▶ on a task that already has
  a session carries on from where it left off.
- **Work sessions** lists your sessions with the time worked, the session running now at
  the top. Open it by tapping anywhere across SESSIONS, WORKED TODAY and TOTAL WORKED
  under Task Stats, or with the list button beside ADD TASK. **CONTINUE** picks a logged
  one back up.
- **Changing a session:** tap its name to open the task, where you can change the title,
  the description, the target and the hours logged on that session. It corrects the
  session that is already there; it never adds another one. The box beside the date ticks
  that session's task off, and **ADD TASK** adds a task without leaving the window.
- **Breaks:** a new install reminds you to take one every hour and gives you ten minutes
  when you do; both are set in Options. The reminder is a window that makes no sound and
  goes away on its own after half a minute, and a second one says when the break is over
  and the timer is counting again. Ending a break yourself with **RESUME** says nothing:
  you are already back.
- **Everything still to do** is listed under **SCHEDULED**, with its due date, its target
  and **START** to put it on the timer. Ticked-off work drops to the bottom under
  **COMPLETED**. Every row says how far it got: the one on the timer counts up beside
  "Active now" as you work.
- **Calendar:** the calendar button next to ADD TASK shows which days have tasks. Tap a
  day to see its tasks; tap the same day again to add a task on it.
- **COMPLETED** (under Task Stats) hides or shows finished tasks in Up Next. They stay
  saved and counted either way.
- **Deleting a task** asks first, and removes its sessions too. Undo brings both back.
- **TASK MANAGER** in the top bar opens Windows' own Task Manager. Windows usually asks
  for permission on its own screen first; it needs the bridge running.
- **Sound:** the output name in the top bar and **Sound Source** both let you pick an
  output. **Switch Sound** moves to the next one.
- **Movie Mode** dims the whole dashboard. Tap anywhere to bring it back.
- **Lock** locks the PC straight away. **Shut Down** and **Restart** only work if you
  press and hold for a second and a half while the bar fills. Let go early and nothing
  happens. Windows can still ask to close apps, and you can still cancel.
- **Status (bottom right):** "EVERYTHING LOOKS GOOD." until CPU, GPU or RAM stays at 90%
  or more for ten seconds, or a reading needs setting up.
- **Options** (top right) has the clock format, Movie Mode brightness, Open iCUE and Reset
  all data. Colours and reading sources are in iCUE (steps 2 and 3).

## Troubleshooting

**Parts of the dashboard say the bridge is needed.**
The bridge isn't running. Restart your PC. If that doesn't fix it, run the installer
again.

**A reading shows "N/A".**
Nothing on this PC reports it. For CPU, GPU or RAM, set a source in iCUE under
**Widgets → Cave Redline Edge → System Readings** (step 3). For the network reading,
install the bridge (step 4). If the note says a connection isn't connected, set
**Network Source** back to Automatic, or to the connection you use (step 3).

**Swiping moves the dashboard but the page doesn't change.**
Set Previous Display Screen and Next Display Screen in iCUE Screen Setup (step 5).

**Two browser tabs are playing but I can only control one.**
Browsers report all their tabs to Windows as a single media source. Media playing in
different apps (for example Spotify and a browser) can be switched between.

**Shut Down or Restart does nothing when I tap it.**
They need a press and hold of a second and a half, so they can't be triggered by
accident. Keep your finger on the button until the bar is full.

**The dashboard's background looks faded.**
Set **Background Transparency** back to 100% in iCUE under **Widgets → Cave Redline Edge**.
It only ever fades the background, never the text or buttons.

**The notification button.**
Tap the bell to open the Windows notification centre, and tap it again to close it.

**The notification bell has no number.**
Some Windows setups don't allow apps to read the notification count. The bell still
opens your notifications, and tapping it again closes them.

## Removing the bridge

1. Find **CaveRedlineEdgeBridge-Setup.exe** (usually in your Downloads folder).
2. Hold **Shift**, right-click it, and choose **Copy as path**.
3. Press **Windows key + R**, paste, type a space and `--uninstall` after it, then press
   **Enter**.
4. Confirm. The bridge is stopped and removed, and no longer starts with Windows.

## Help

Questions or problems: <https://github.com/Caveproduction-bot/cave-redline-edge/issues>
