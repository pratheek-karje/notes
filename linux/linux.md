# linux

## print cpu frequency

`cat /sys/devices/system/cpu/cpu*/cpufreq/scaling_cur_freq`

## add new group to an user & use new group without re-login

[link](https://superuser.com/a/345051)
ex:
  current user: user1
  new group: group2
  run: `sudo usermod -aG group2 user1`
  to work with new group without relogin, start new shell like this:
    `newgrp group2`

## network

`ip address show`

`ip -4 -br a` show minimal information

`ip routes`

`bridge link`

## other

`cp -L my-symbolic-link /my/path`: copy content of symbolic link

## alias

alias clr='clear'
alias d='docker'
alias k='kubectl'
alias g='git'
alias wl='nmcli d wifi list'
alias wcon='nmcli d wifi connect'
alias n='nvim'

## bash prompt options (PS1>)

\a – A bell character
\d – Date (day/month/date)
\D{format} – Use this to call the system to respond with the current time
\e – Escape character
\h – Hostname (short)
\H – Full hostname (domain name)
\j – Number of jobs being managed by the shell
\l – The basename of the shells terminal device
\n – New line
\r – Carriage return
\s – The name of the shell
\t – Time (hour:minute:second)
\@ – Time, 12-hour AM/PM
\A – Time, 24-hour, without seconds
\u – Current username
\v – BASH version
\V – Extra information about the BASH version
\w – Current working directory ($HOME is represented by ~)
\W – The basename of the working directory ($HOME is represented by ~)
\! – Lists this command’s number in the history
\# – This command’s command number
\$ – Specifies whether the user is root (#) or otherwise ($)
\\– Backslash
\[ – Start a sequence of non-displayed characters (useful if you want to add a command or instruction set to the prompt)
\] – Close or end a sequence of non-displayed characters

