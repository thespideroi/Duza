# Duza the Cubic Vessel
Convert your YuGiOh cubes on YGOPRODeck or cube.yugioh-api into a format usable on Draftmancer, and convert your draft pool back into a YDK

**If you're only here for playing someone else's cube, you can read the [Installation](#installation) section and then skip straight to the [Deck Conversion](#deck-conversion) section.**

[Keep up to date on what is planned/already completed for Duza](https://docs.google.com/spreadsheets/d/1te0DBEgWNEuUR3ICaJeC4Dz-2RAo28iY0bhJe4yqtwI/edit?usp=sharing)
## Table of Contents
1. [Installation](#installation)
2. [Cube Conversion](#cube-conversion)
3. [Using Draftmancer](#using-draftmancer)
4. [Deck Conversion](#deck-conversion)
5. [Options and Debug](#options-and-debug)

## Installation
- **For Windows Users**: A compiled executable is available! Unfortunately, It is too large to be distributed via Github — It is available for Download on the [YuGiOh Cube Discord](https://discord.gg/b72Tgva7gh) however.
  - Text fields may not be responsive upon first launch of the executable — If this happens, select a file import button, then cancel the import. This should fix the issue.
- **For Non-Windows Users**: You will have to compile Duza yourself! Duza requires `numpy`, `pandas`, and `requests`, and was written on Python 3.8.

## Cube Conversion
1. To convert your cube into Draftmancer format, you will first need to download it from whatever site it's hosted on.
   - **From YGOPRODeck** — Navigate to the cube's view page and click the `Download Cube (.csv)` button, or the `Export Cube (.csv)` from the cube's edit page.
   - **From cube.yugioh-api** — Navigate to either the cube's view or edit page, and click the `Download` button. This will download the cube as a TXT file.
   - Duza also accepts YDK files as input.
2. Launch Duza, and navigate to the `Cube Translator` page.
3. Select `Import File`, and load the file for your cube. If your cube was in CSV format, it will be converted to and displayed as a YDK-like format.
4. Select `Export Draftmancer`. Name your file and save it to your machine.

## Using [Draftmancer](https://draftmancer.com/)
1. At the end of the second bar from the top of the tab, select `Settings`.
2. Scroll to the bottom of the pop-up and select `Upload a Custom Card List file by dropping it here or by clicking to browse your computer.` Upload your cube file.
3. Once the cube uploads, you can close the Settings window. The Set dropdown should be replaced with `Cusom Card List`, and a blue button to its right to confirm that the cube was uploaded properly — It may take a moment for all of the card images to load.

## Deck Conversion
1. After drafting your deck on Draftmancer, Select `Export > Card Names`. Draftmancer will copy your deck to the clipboard.
2. Launch Duza — If you had already launched it, navigate to the `Deck Translator` page.
3. Paste your deck into the text field. Drafmancer might have tried to add some Basic Land cards at the bottom of your decklist — If it did, delete those lines.
4. Select `Export YDK` or `Export YDKe`. If saving a YDK, name your file and save it to your machine. Upload to your dueling platform of choice!

## Options and Debug
### Options
- Currently, the only feature of the options menu is to update Duza's database. Duza will automatically refresh its database if it's 30 days out-of-date, but you can select this to force an update.
### Debug
- The debug menu has a text field for searching up a card name's passcode, or the card that a passcode corresponds to. If a translator has trouble recognizing a card, you can use this menu to confirm what passcode/name Duza uses in its database — Duza's database is downloaded from YGOPRODeck; report any incorrect passcodes to them!
