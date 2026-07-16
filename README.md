# Velocity

Velocity is a beautiful, modern & opinionated Linux distribution — a soft fork of [Omarchy](https://omarchy.org) by DHH, evolving toward an AI-ready desktop.

Open source. Not a commercial product.

## Command line

Prefer the Velocity entrypoint:

```bash
velocity update
velocity theme list
velocity commands
```

`omarchy` still works as a compatibility alias (same command center). Install paths remain under `~/.local/share/omarchy` for soft-fork compatibility.

## Attribution

Velocity is based on [Omarchy](https://github.com/basecamp/omarchy) by DHH / Basecamp. Thank you for the foundation.

## License

Velocity is released under the [MIT License](https://opensource.org/licenses/MIT), same as Omarchy.

## Upstream merges

Velocity tracks Omarchy as a soft fork. Keep remotes like this:

```bash
git remote add upstream https://github.com/basecamp/omarchy.git   # once
git remote -v
# origin    -> https://github.com/OpenChatGit/velocity (what `velocity update` pulls)
# upstream  -> https://github.com/basecamp/omarchy
```

Bring upstream changes in deliberately:

```bash
git fetch upstream
git merge upstream/master   # or upstream/dev — match their default branch
# resolve conflicts, especially branding files (logo.txt, icon.txt, README, fastfetch, limine, plymouth, sddm, sessions)
git push origin HEAD
```

Installed systems update from **your** `origin`. If `origin` still points at Basecamp, `velocity update` will overwrite Velocity branding with Omarchy.
