# blinkto
A simple code sync tool to build your stuff on a remote server. If you're like me, your laptop may not have all the juice in the world, but you might own a server or desktop that _does_. `blinkto` will help you take your local `git` repositories and sync them to another machine over SSH. Anytime you change a file, it will pick it up and sync it quickly. You can then run build commands on the server, freeing up CPU on your laptop to run all those chat clients.

# Configuration
I hope to use a simple config file (yaml/json/toml) so making adjustments is easy. 

# CLI
The cli should be simple and intuitive. Allowing for the dynamic additions of workspaces and simple error messages.

A simple run without a config.
```sh
$ blinkto bob@fastserver.com:~/remote_project_dir --project my_project_dir/ --exclude=.vscode,node_modules
```

# Warnings
This is a ONE-WAY sync. Local -> Server only. Not the other way around. So don't make precious changes on your remote while `blinkto` is running or you risk clobbering your work.

# Extras (maybe someday)
It would be completely awesome to have a mode that doesn't just log the state of syncronizations, but displays them in a terminal UI kind of way. Think [webpack-dashboard](https://github.com/FormidableLabs/webpack-dashboard), but maybe a little more simple and stripped down. Maybe use something like [tui-rs](https://github.com/fdehau/tui-rs)
