# Fieldbook — farm records classroom prototype

A self-contained teaching activity inspired by farmOS recordkeeping concepts. This is an independent educational prototype, not a farmOS installation or a replica of its interface. It has no connection to a farmOS server.

## Included learning workflow

- Review simulated pistachio (22 acres) and garlic (2 acres) fields.
- Add and edit fields and link observations or activities to each field.
- Enter soil moisture, bulk EC, temperature, irrigation, scouting, planting, harvest, or other records.
- Preserve dates, values, units, sample location IDs, depth, optional WGS 84 latitude/longitude, methods, and notes.
- Identify records as Actual, Simulated, or Planned.
- Search records and filter by field.
- Complete the built-in Student mission and reflection.
- Export a readable HTML report for Canvas, a CSV table for Excel/QGIS, and a complete JSON backup.
- Restore a backup or clear a shared-computer workspace after saving work.

The layout sketch is illustrative. It is not a geographic map, does not change with field edits, and does not display coordinates. Field and sample examples are invented for teaching. Editing a starter record preserves its example label; students should create their own records.

## How student work is stored

Each browser has its own workspace using localStorage. Students do not need GitHub accounts to open the published page. Entries are not posted to GitHub, emailed to the instructor, synchronized among students, or sent to Canvas. A shared browser profile means a shared workspace. Use separate browser profiles or download, verify, and clear work between students.

Storage can be erased by clearing browser/site data, private browsing, browser restrictions, or device changes. If storage is blocked or full, a message tells the student to download a backup. Students should save a JSON backup each session and restore it on the next device. Import replaces all current data after confirmation; it does not merge records. Backups have a 10 MB import limit; the prototype supports up to 100 fields and 5,000 records.

CSV includes starter examples, source labels, and an explicit `starter_example` column. A report also labels examples and reports the student-record count separately. The CSV uses UTF-8 and includes EPSG:4326 for coordinate-bearing records. It is not a native farmOS import format. Numeric entries require units; coordinate pairs must be complete and within geographic ranges. Scientific plausibility and measurement comparability still require student/instructor review.

## Suggested classroom use

Ask students to create three separate soil observations (moisture, bulk EC, temperature) and one activity record, then write a management question, evidence-based interpretation, limitation, and next measurement. Measurements at one location should use the same location ID. For simulated data, choose Simulated and identify the practice dataset as the source. For a proposed operation, choose Planned and explain in the notes that it has not occurred.

Students download the HTML report and CSV to submit to Canvas; retain JSON as a backup. The report opens in a browser and can be printed/saved as PDF. The checklist checks presence, not correctness. Reports and backups are editable and do not prove identity, attendance, equipment competency, or fieldwork.

## Limits and next steps

This version is intended for recordkeeping practice. It does not include real student logins, a shared class database, live maps, automatic GPS collection, photos, sensor connections, authenticated audit trails, agronomic recommendations, or native farmOS API integration. It has no classroom-hours lock.

For a genuinely shared multiuser farmOS workflow, use a server-hosted farmOS instance with accounts and permissions. GitHub Pages serves this standalone teaching interface; it does not supply the server/database functionality of farmOS.

The application uses semantic HTML, labeled controls, keyboard-operable dialogs, visible focus states, and text equivalents to the schematic. Its layout adapts to small screens. Conduct your institution's accessibility review and a student-device pilot before broad use.

## Verification performed

Checked in a desktop browser: creating and editing observations; missing-unit validation; search; persistence after reload; adding a field; student identity/reflection; progress checklist; reset to examples. Programmatic checks covered JavaScript syntax, backup round-trip validation, invalid dates/coordinates/field references/duplicates, CSV formula protection, and HTML escaping. Mobile styles are included; physical phone and Chromebook testing has not been performed.

Version 1.0. No external scripts or tracking code.
