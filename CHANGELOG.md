# Changelog

## 1.0 (2026-10-28)
- First release. Once per game launch, a few seconds after you're in control, a subtitle shows which IV-SDK .NET
  and GTA IV versions are running (read live from the files). On GTA IV 1.2.0.59 it adds "(Unofficial 1.2.0.59
  Beta)". The same line goes to the IV-SDK .NET console (F4) and log.
- Waits until no subtitle, help message or conversation is on screen, so it never covers dialogue or mission text.
- Uses IV-SDK .NET's own `IVGame.ShowSubtitleMessage` (a literal string), so none of the game's text is changed.
  (A pre-release test build overwrote the game text entry `PLACEHOLDER_1`, which only has room for 35 characters;
  that was dropped before release.)
