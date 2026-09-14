# scripts

Personal scripts, organized by profile so the right set ends up on `PATH` depending on which
machine or context I'm on.

- `general/` — scripts usable everywhere, regardless of profile.
- one directory per profile (currently `melt`, `grem`) — scripts specific to that profile only.
- `dist/` — generated, gitignored. One directory per profile, each filled with symlinks to
  every script in `general/` plus that profile's own. A profile's script overrides `general`'s
  of the same name.

Run `./make_dist` to (re)build `dist/`, then put `dist/<profile>` on `PATH`.

A new profile needs nothing but a new top-level directory — `make_dist` picks up any directory
other than `general` and `dist` automatically.
