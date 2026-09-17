# Sale Scout — releases

This repository only exists to host update files. Customers never visit it —
their copy of Sale Scout quietly reads `latest.json` to see whether a newer
version exists.

**This folder is the one connected to GitHub.** Keep working in here.

## Publishing a new version

Ask Claude: **"publish a new Sale Scout version"** and it does steps 1–3 for you.

1. **Bump the version number** in the skill's `scripts/version.py`
   (e.g. `1.0.0` → `1.1.0`).

2. **Build the zip** into this folder, named `sale-scout-1.1.0.zip`.

3. **Update `latest.json`** in this folder:

   ```json
   {
     "version": "1.1.0",
     "url": "https://raw.githubusercontent.com/stefaniebecker/sale-scout-releases/main/sale-scout-1.1.0.zip",
     "notes": "One short sentence about what changed."
   }
   ```

4. **You do this part:** open GitHub Desktop, type a short summary, click
   **Commit to main**, then **Push origin**.

Everyone who owns Sale Scout sees the update the next time they run the
check-up, and can install it by asking Claude to update Sale Scout.

## Version numbers

Three numbers: `1.1.0`. Middle one for new features, last one for small fixes.
The updater only offers an update when the published number is higher than the
customer's.

## Keep old zips

Don't delete previous versions. Anyone mid-download, or on a slow connection,
may still be reaching for them.
