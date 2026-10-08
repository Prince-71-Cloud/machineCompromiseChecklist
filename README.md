# Machine Compromise Checklist

A self-assessment checklist that helps software engineers check their own machine for signs of compromise, malware or unauthorized access.

It is a single HTML page: no build step, no install, no data leaves your browser.

**Live site:** https://prince-71-cloud.github.io/machineCompromiseChecklist/

## How to use

1. Open the [live site](https://prince-71-cloud.github.io/machineCompromiseChecklist/), or open `machine-compromise-checklist.html` in any web browser.
   - Locally: double-click the file, or run `xdg-open machine-compromise-checklist.html` (Linux) / `open machine-compromise-checklist.html` (macOS) / `start machine-compromise-checklist.html` (Windows).
   - Or clone the repo first:
     ```bash
     git clone https://github.com/Prince-71-Cloud/machineCompromiseChecklist.git
     cd machineCompromiseChecklist
     ```
2. Pick your operating system tab: **Linux / Kali**, **macOS** or **Windows**.
3. Work through each section. Every item gives you:
   - a **command** to run in your terminal (or PowerShell on Windows), and
   - a **red flag**: what suspicious output looks like.
4. Copy the command, run it on your own machine and compare the output against the red flag.
5. If anything looks wrong, follow the **What If You Find Something?** steps at the bottom of the page.

> Run these commands only on machines you own or are authorized to inspect. Some checks need `sudo` / Administrator rights.

## What it covers

| OS | Sections |
|----|----------|
| Linux / Kali | User accounts & login activity · Network & connections · Processes & services · Files & permissions · System files & integrity |
| macOS | User accounts & login · Network & connections · Processes & malware · Files & SSH keys |
| Windows | User accounts & logins · Network & connections · Processes & services · Files & registry |

The page also includes:

- **What If You Find Something?** Isolate the machine (keep it running), snapshot it, document everything, alert your security team and stop using it for work until forensics is done. Don't shut it down abruptly: that can destroy evidence.
- **Prevention Going Forward.** Patch regularly, use a password manager and MFA, rotate API keys, use a VPN on public Wi-Fi, disable SSH password auth, review cron jobs and never commit secrets.

## Notes

- Fonts load from Google Fonts. Offline, the page still works with fallback system fonts.
- The site is served by GitHub Pages from the `main` branch. `index.html` redirects to the checklist page.
