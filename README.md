# Redtimer

Redtimer is a [Pomodoro timer](https://en.wikipedia.org/wiki/Pomodoro_Technique) for Bash which makes use of [`at`](https://tldr.inbrowser.app/pages/common/at) and [`notify-send`](https://tldr.inbrowser.app/pages/linux/notify-send).

Started as a script in my [script-fu](https://github.com/clobrano/script-fu/blob/master/redtimer) repository, I decided to give it a dedicated place for visibility.

## Installation

Just download the script and make it executable:

```bash
curl https://raw.githubusercontent.com/clobrano/Redtimer/main/redtimer -o redtimer
chmod +x redtimer
```

## Usage

```
##    redtimer help           Show this message
##    redtimer work [min]     Start work session
##    redtimer pause [min]    Take a break
##    redtimer end            Stop redtimer
##    redtimer log [search]   Show redtimer log, eventually filtered by search term
##    redtimer                Show running redtimer

# Time duration setting hierarchy:
# 1. user input if provided
# 2. environment variables if set
# 3. script defaults

# environment variables
_work_session_time=${REDTIMER_WORK_SESSION_TIME:-35}
_pause_session_time=${REDTIMER_PAUSE_SESSION_TIME:-10}
_log_session_path=${REDTIMER_LOG_SESSION_PATH:-~./redtimer-session-log.txt}
```
