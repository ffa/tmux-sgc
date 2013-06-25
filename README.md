# Save your tmux sessions and their states

### status: beta

### simple.
  `tsgc save`    saves all tmux sessions
  `tsgc list`    lists all saved tmux sessions
  `tsgc restore <session name>`    restores the tmux session "<session name>"

### complete save
  * save history buffer
  * save bash command history
  * save tmux paste buffer
  * save tmux sessions', windows', and panes' layouts
  * save tmux options: global, server, session, and window
  * TODO: save tmux environment settings

### open
  edit your generated session files using bash and tmux; no new commands or
  languages to learn. The goal is to help manage your sessions by automating
  tasks. The session files are generated for your direct use and portability.


## How it works

  the `save` command generates a ".tmux.sessions" folder in the current working
  directory. For each session, a folder is created with the session name in 
  ".tmux.sessions". In the folder, a bash "session" executable stores the list
  of tmux commands to restore the session. In the same folder, plain text files
  are used to store data, like command history, paste buffer, and history
  buffer. Finally, the ".tmux.conf" file stores all of tmux's options, global, 
  server, session, and window, and is the configuration file loaded in tmux, 
  with the "-f" option. So, your "~/.tmux.conf" will not be loaded for restored
  sessions.


## Contribute

  Help is encouraged. Hack and contribute back. Create issues.

### Developers

  The code is slightly messy, I know. I have difficulty beautifying bash. Help,
  patches, and recommendations are wanted.

  testing and bugfixes are the priority.

  And, other contributions are welcome.

  #### standards: ####
  * the 80 width limit
  * comment
  * maintain the indentation
  * the "--debug" option is available to help in the extermination


## TODO

  * save environmental variables, tmux
  * Better organize session data: ".historyBuffer" and ".bashHistory"
  * real "--help" options
  * plugin capability, so other shells, like zsh and fish, may be used instead
    of bash


## Credits

  * ffa
  * thank you rbenv team for the command pattern code
