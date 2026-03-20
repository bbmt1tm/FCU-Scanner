FCU SCANNER — USER GUIDE
========================
DXR2 Serial Number Capture Tool
Version: see home screen

------------------------------------------------------------------------
OVERVIEW
------------------------------------------------------------------------
FCU Scanner is a mobile web app for capturing Siemens DXR2 controller
serial numbers on site. Load your FCU spreadsheet, scan each controller's
barcode with your phone camera, and export the completed spreadsheet when
done. All data is saved locally on your phone — no internet required
once the app has loaded for the first time.


------------------------------------------------------------------------
FIRST TIME SETUP
------------------------------------------------------------------------

ON SAMSUNG INTERNET (Samsung phones):
1. Open Samsung Internet on your phone
2. Go to:  https://[your-github-username].github.io/fcu-scanner
3. The app will load and cache itself for offline use
4. To install to home screen:
   - Tap the three-line menu button (bottom right)
   - Tap "Add page to"
   - Tap "Home screen"
   - Tap "Add"
   - The FCU Scanner icon now appears on your home screen

ON CHROME (Android):
1. Open Chrome on your phone
2. Go to:  https://[your-github-username].github.io/fcu-scanner
3. The app will load and cache itself for offline use
4. To install to home screen:
   - A banner may appear at the bottom saying "Install FCU Scanner"
   - Tap "Install" on that banner, OR
   - Tap the three-dot menu (top right) > "Add to Home screen"
   - Tap "Add"
   - The FCU Scanner icon now appears on your home screen

NOTE: After the first load over WiFi the app works completely offline.
No internet connection is needed on site.


------------------------------------------------------------------------
LOADING YOUR SPREADSHEET
------------------------------------------------------------------------

Your spreadsheet should have the following columns (names can vary):
  - FCU Reference    e.g. FCU-1110001
  - Location         e.g. Boardroom (room name and number on separate
                     lines within the same cell)
  - Serial Number    (blank — to be filled in by scanning)

Multiple sheets (floors/levels) in one .xlsx file are fully supported.
All sheets are merged into one list and the sheet name is used as the
floor filter.

STEPS:
1. Open the app — you will see the FCU Scanner home screen
2. Tap "Load Spreadsheet"
3. Navigate to your .xlsx or .csv file in phone storage and tap it
4. The app shows a column mapping screen — check that:
   - "FCU Reference column" points to your FCU ref column
   - "Location column" points to your room/location column
   - "Serial Number column" points to your serial number column
   The app will auto-detect these from the column headers.
   A note at the top will confirm how many sheets/floors were found.
5. Tap "Confirm & Continue"
6. Your full FCU list appears, ready to scan


------------------------------------------------------------------------
USING THE FCU LIST
------------------------------------------------------------------------

THE LIST:
- Each row shows the FCU reference, room number (amber badge) and
  room name
- Green tick = serial number already captured
- Empty circle = not yet scanned
- The progress bar at the top shows overall completion across all floors

SEARCHING:
- Use the search bar to filter by FCU reference, room name or room number
- The number pad below the search bar lets you type quickly with one
  hand — tap digits to narrow the list without the keyboard appearing
- DEL removes the last digit, CLR clears the whole search

FILTERING BY FLOOR:
- If your spreadsheet has multiple sheets (floors), filter chips appear
  below the search bar — e.g. "Level 01", "Level 06"
- Tap a chip to show only that floor
- Combined with the number pad: select a floor then type digits to find
  a specific FCU on that floor quickly

HEADER BUTTONS:
  Home    — returns to the main screen (resume option will be shown)
  Save    — saves a progress file (.fcusave) to your phone Downloads
  Export  — exports the completed spreadsheet back to your phone


------------------------------------------------------------------------
SCANNING A SERIAL NUMBER
------------------------------------------------------------------------

1. Tap any FCU in the list to open the scan screen
2. The FCU reference and room details are shown at the top
3. Point your camera at the barcode on the DXR2 controller
   - The barcode is on the white label on the outside of the unit
   - Align it within the orange corner brackets
   - The app scans continuously — no need to tap anything
4. When a barcode is detected:
   - The phone vibrates once
   - The serial number appears in the amber box
   - "Confirm Serial" button appears
5. Check the serial number matches what is printed below the barcode
   on the label (e.g. 140015A80E)
6. Tap "Confirm Serial" to save it
7. The app returns to the FCU list — the FCU is now marked green

IF THE SCAN DOESN'T WORK:
- Tap "Retry" to scan again
- Make sure the label is clean and well-lit
- Type the serial manually in the text box at the bottom of the screen
  then tap "Confirm Serial"

DUPLICATE WARNING:
- If the scanned serial already exists on another FCU a warning will
  appear showing which floor and FCU reference it belongs to
- This usually means the wrong controller was scanned
- Tap "Cancel — rescan" to try again, or "Save anyway" to override

FCU ALREADY HAS A SERIAL:
- If an FCU already has a serial number, the current serial is shown
  in a red box at the bottom of the scan screen
- You can scan a new barcode to replace it — a confirmation prompt will
  show the old and new serials before saving
- Or tap "Clear" to remove the serial entirely (also requires
  confirmation)


------------------------------------------------------------------------
SAVING YOUR PROGRESS
------------------------------------------------------------------------

AUTOMATIC (happens silently after every scan):
- The app saves all progress to your phone's browser storage after
  every confirmed serial
- A small dot in the header shows green when saved, amber while saving
- The timestamp updates to show when it was last saved
- This survives: closing the browser, restarting the phone, losing
  signal

MANUAL SAVE TO FILE (recommended at end of each day):
- Tap the blue "Save" button in the header
- A .fcusave file is saved to your phone's Downloads folder
  e.g. BuildingX_FCUs_progress_2026-03-20.fcusave
- This is a complete snapshot of all progress
- Keep this as your daily backup
- Can be shared with a colleague via WhatsApp, email, etc.

NOTE: If Chrome's site data is cleared, browser autosave is lost.
The .fcusave file is your safety net against this.


------------------------------------------------------------------------
RESUMING A SESSION
------------------------------------------------------------------------

AUTOMATIC RESUME (same phone, browser data intact):
1. Open the app (from home screen icon or browser)
2. The home screen shows a blue "resume" card with the project name,
   last save time and progress bar
3. Tap "Resume →" to continue where you left off

LOADING A PROGRESS FILE (different phone, or after clearing data):
1. Open the app
2. Tap "Load saved progress file (.fcusave)"
3. Navigate to the .fcusave file and tap it
4. All progress is restored exactly as it was saved

STARTING FRESH:
- On the resume card tap "Discard" (requires confirmation)
- Then load a new spreadsheet as normal


------------------------------------------------------------------------
EXPORTING THE COMPLETED SPREADSHEET
------------------------------------------------------------------------

1. Tap the amber "Export" button in the header
2. The updated spreadsheet is saved to your phone's Downloads folder
   e.g. BuildingX_FCUs_updated.xlsx
3. The file has the same structure as the original — all sheets intact,
   serial numbers filled in
4. Share it back to the office via email, WhatsApp, Teams etc.

NOTE: You can export at any point — partially completed is fine.
Blank serial cells stay blank in the exported file.


------------------------------------------------------------------------
TIPS FOR ON-SITE USE
------------------------------------------------------------------------

- Install to home screen before going on site so it works offline
- Do a manual Save (.fcusave) at the end of each floor/session
- If handing over to a colleague mid-job, send them the .fcusave file
  and they can load it on their own phone
- The room number (amber badge) matches the canonical room number on
  your layout drawings — use this to cross-reference location
- Use the floor filter chip + number pad combination to jump quickly to
  a specific area without typing
- If a serial number looks wrong after confirming, tap the FCU in the
  list to re-enter — you will be asked to confirm the replacement
- Serial numbers on DXR2 controllers are printed below the barcode
  in the format: S/N  140015A80E  Hex


------------------------------------------------------------------------
TROUBLESHOOTING
------------------------------------------------------------------------

App not updating after a new version is deployed:
- Close the browser completely (swipe away from recents)
- Reopen and reload the page
- Or go to: [your-url]?bust=1.9 to force a fresh load

Resume option not showing after pressing Home:
- This is fixed in v1.9 — update to the latest version

Barcode not scanning:
- Ensure you are using Samsung Internet or Chrome on Android
- iPhones do not support barcode scanning — use manual entry
- Clean the label and ensure adequate lighting
- Try tilting the phone slightly — sometimes an angle helps with
  reflective labels

Wrong data in serial number column after loading:
- This happened on older versions where sheets had different column
  orders — fixed in v1.6+
- Ensure you are running the latest version (check home screen)

File not loading after discarding and reselecting:
- Fixed in v1.3+ — update to the latest version


------------------------------------------------------------------------
SUPPORT
------------------------------------------------------------------------
App developed for internal use.
For issues or feature requests raise with your BMS project lead.
