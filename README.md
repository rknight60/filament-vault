# Filament Vault

A simple iPhone-first PWA for identifying vacuum-bagged 3D-printing filament with NFC tags.

## Data model
- Material: PLA, PLA+, PETG, TPU, Unknown
- Colour
- Brand (optional)
- Photo (optional)
- Notes (optional)
- FIL ID generated automatically

Data is stored in the browser's local storage on the iPhone. No account or database is required.

## NFC workflow
Use an existing NFC-writing app to write the URL shown by **NFC URL** for a filament record. The URL contains only the record ID. When the iPhone opens the URL from an NFC scan, Filament Vault displays that record.

## Hosting
The app must be served over HTTPS for reliable iPhone Home Screen/PWA behaviour. A static host such as GitHub Pages can host these files for free. The host contains only the application; filament records remain local to the iPhone.

## Important limitation
If Safari website data for the app is deleted or the phone is restored without a backup, local records can be lost. Use Export Backup periodically. A future version can add a more robust backup/restore flow.
