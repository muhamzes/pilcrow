# Screenshots

Mostly generated rather than hand-captured — regenerate with `npm run shoot`
against a running dev server. Committed so the look can be reviewed in a pull
request without anyone having to run the app.

| | |
| --- | --- |
| `riso-light-*` | the default theme, and the design target (`docs/mockups/05-riso.html`) |
| `riso-dark-*` | the same structure at night |
| `default-light-*` | a second preset, as evidence the Riso treatment is contained |

Four are hand-captured, because they need a signed-in session and a thread with
real content in it: `chat.png`, `model-selector.png`, `admin-providers.png` and
`long-thread.png`. These are the four the README leads with, for readers who
cannot sign in to the deployment. `shoot` does not produce them and will not
overwrite them. What to check before committing one is in the
[README](../../README.md#screenshots) — they are taken while authenticated.

```bash
npm run shoot                        # riso, light
npm run shoot -- --theme=default     # any preset
npm run shoot -- --scheme=dark
npm run shoot -- --scale=2           # retina; ~4x the file size
```

`shoot` also fails (exit 1) on three things a screenshot alone will not tell
you: a console or hydration error, both theme copy variants rendering at once,
and Riso-only markup leaking into another theme. All three have happened.

1x by default: Riso's paper grain is per-pixel noise and does not compress, so a
2x capture of it is 1.8MB against 450KB.
