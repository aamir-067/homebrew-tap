# aamir-067/homebrew-tap

Homebrew formulae by [aamir-067](https://github.com/aamir-067).

## macscan

[macscan](https://github.com/aamir-067/macscan-cli) is a deep, read-only security scanner for macOS: malware, infostealers, persistence, browser extensions, developer and AI tool configs, supply-chain attacks, YARA and ClamAV.

```bash
brew install aamir-067/tap/macscan
macscan-setup          # installs or upgrades the scanner; asks for your password
```

Then give Full Disk Access to `/usr/local/mac-triage/bin/macscan-helper` when asked, and run `macscan`.

**Why two steps?** macscan runs as root, so its files must live in a root-owned folder (`/usr/local/mac-triage`). Homebrew's own folders are writable by your user account, which would let other programs change what root runs. Homebrew downloads and verifies the release installer; `macscan-setup` runs it with `sudo`.

**Upgrade:** `brew upgrade macscan && macscan-setup`, or `macscan --update`.
**Uninstall:** `macscan-setup --uninstall`, then `brew uninstall macscan`.
