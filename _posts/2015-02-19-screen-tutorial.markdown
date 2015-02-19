---
layout: post
title:  "Screen Tutorial"
date:   2015-02-19 01:46:42
comments: true
---

GNU Screen is a software application that can be used to multiplex several virtual consoles, allowing a user to access multiple separate terminal sessions inside a single terminal window or remote terminal session. It is useful for dealing with multiple programs from a command line interface, and for separating programs from the Unix shell that started the program.

# Install
	sudo apt-get install screen


# Commands to start screen
	screen
	screen -S <name>	# Start a new screen session with session name
	screen -ls 			# List running sessions/screens


# Common commands while in a screen

- `Ctrl+a c  `: Create a new window
- `exit      `: Exit from the window
- `Ctrl+a "  `: List all windows
- `Ctrl+a d  `: Detach from the screen

# Reattach to the screen
	screen -r <<Name of Screen>>

# Resources
- [Screen Quick Reference](http://aperiodic.net/screen/quick_reference)
- [Digital Ocean Screen Tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-screen-on-an-ubuntu-cloud-server)
