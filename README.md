# amesHyprland

A modification of eshrh's [ames](https://github.com/eshrh/ames) script to work with Hyprland.

## Changes

- uses [wl-clipboard](https://github.com/bugaevc/wl-clipboard) to fetch clipboard contents
- uses [slurp](https://github.com/emersion/slurp) and [grim](https://gitlab.freedesktop.org/emersion/grim) to take interactive screenshots
- uses [grimblast](https://github.com/hyprwm/contrib/tree/main/grimblast) to take screenshots of the active window
- uses [pw-record](https://linuxcommandlibrary.com/man/pw-record) to record audio ([by WilsonNet, fixes issue 15](https://github.com/eshrh/ames/issues/15#issuecomment-2456144139))
- starting and stopping audio recording sends a signal to [waybar](https://github.com/Alexays/Waybar), which can be used to update waybar modules. see the [custom module page](https://github.com/Alexays/Waybar/wiki/Module:-Custom) in the waybar wiki for more information, or [here](https://github.com/balfiere/RecordAudioOutputHyprland?tab=readme-ov-file#how-to-use) for an example of how to create a waybar module that appears when audio is recording.
- adds an optional second sentence field. when `ames.sh -c` is run, if `SENTENCE_FIELD_2` is a non-empty string then the clipboard is sent to both `SENTENCE_FIELD` and `SENTENCE_FIELD_2`. useful for those using an addon like [Japanese Readings and Pitch Accent](https://ankiweb.net/shared/info/1845503807) where one field will be modified.