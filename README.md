# `posix-pomo` - CLI Pomodoro timer 

`posix-pomo` is a simple POSIX-compliant shell script that implements a pomodoro timer for Linux and the BSDs.

![posix-pomo demo in a GIF](https://aedrielkylejavier.me/assets/posix-pomo.gif)
*made with [VHS](https://github.com/charmbracelet/vhs)*

![posix-pomo notifications image 0](https://aedrielkylejavier.me/assets/posix-pomo-notif0.png)
![posix-pomo notifications image 1](https://aedrielkylejavier.me/assets/posix-pomo-notif1.png)
*example notifications using the `dunst` notification daemon on Arch Linux (btw)*

## features

- **customizable durations**: supports specifying the duration of work and break intervals in hours, minutes, or seconds.
- **cli progress bar**: displays a progress bar in the terminal showing the remaining time. *(built from scratch, no external program/library needed)*
- **notifications**: sends desktop notifications at the end of each session via `notify-send`.
- **sound alerts**: plays a sound alert at the end of each session via `mpv`.

## dependencies

- **mpv**: for playing sound alerts. *(will probably look for something more suckless in the future)*
- **notify-send**: for desktop notifications (should be preinstalled on most distros as part of `libnotify`).
- ensure you have the required sound file (`pomo-sound.mp3`) and icon file (`pomo-tomato.png`) located in the `~/.cache/pomo/` directory.
    * the repo has these files but you can also provide your own files if you'd like.

## installation

1. ensure you have all dependencies installed
2. download the `posix-pomo` script from this repository or clone the whole repo.
3. make the script executable:
   ```bash
   chmod +x posix-pomo
   ```

## usage

to start a timer, use the following syntax:

```bash
./posix-pomo <mode(work/break)> <duration(h/m/s)>
```

- `<mode(work/break)>`: either `work` for work sessions or `break` for break intervals.
- `<duration(h/m/s)>`: the length of the timer, followed by `h` for hours, `m` for minutes, or `s` for seconds (e.g., `25m` for 25 minutes).

### examples

- start a 25-minute work session:
  ```bash
  ./posix-pomo work 25m
  ```
- start a 5-minute break:
  ```bash
  ./posix-pomo break 5m
  ```

## contributing

I honestly don't expect contributions — given how simple this is, but of course, contributions are welcome! If you have suggestions for improvements or bug fixes, please feel free to open an issue or submit a pull request.

## license

distributed under the "unlicense" license. see `LICENSE` for more information.
