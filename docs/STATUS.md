# Status

The refresh review fix for [PR #197](https://github.com/thisisgm/flea/pull/197) preserves an open rename editor and its draft before a directory refresh or search rerun.

Run `tests/js.sh watch` for the background-menu regression and `tests/run-all.sh` for the headless battery. Set `FLEA_FIXTURE_ROOT` to a writable fixture directory outside the home directory on machines without `/home/flea-sandbox`.

The native `tests/ui.sh refresh` check requires `omarchy-drive`. Open review work is listed by `gh pr view 197 --repo thisisgm/flea --comments`.

Validation on 2026-09-24: the regression failed before the guard and passes after it; the full JavaScript battery, debug and release Rust unit suites, QML lint and file-budget checks pass. The headless runner remains red in ops, protocol, thumbs, thumbs-exec, uistate, media and shellload on this machine. The thumbnail suites lack their media fixture; the ops failures also reproduce at the unchanged PR head. No native pointer-driven verification is claimed.
