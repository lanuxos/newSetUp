# vlc.md

## [How to Fix Movies with Loud Action Music and Low Dialogue Volume](https://www.vlchelp.com/fix-movies-loud-music-low-dialogue/)

- Tools > Effects and Filters [CTRL+E]
- Audio Effects > Compressor > Enable
  - RMS/peak    0.0
  - Attack      ~24.9   ms
  - Release     ~262.9  ms
  - Threshold   ~-23.8  dB
  - Ratio       20.0:1
  - Knee radius ~1.5    dB
  - Makeup gain ~7.5    dB
- Save
- Close

## Preferences [CTRL+P] / Keyboard shortcut
- Next                          N
- Previous                      B
- Cycle audio track             A
- Cycle subtitle track          S
- Cycle source aspect ratio     x

## auto launch command
- create start-up command with below command
`vlc -f VIDEO_PATH`

## auto launch command at specified display [no test yet!]
```--qt-fullscreen-screennumber=0`    # 0 is 1st display
- Preferences [CTRL+P] > Video > Fullscreen Video Device
