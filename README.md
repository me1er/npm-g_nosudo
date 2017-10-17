# npm-g_nosudo

A shell script which will fix the problem where you want to stop using sudo for npm -g on Ubuntu.

Inspired by [Sindre Sorhus' Guide](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md)

Tested on Ubuntu 14.04 with Bash

## Usage:

Download the script, run it:
```
wget -O- https://raw.githubusercontent.com/glenpike/npm-g_nosudo/master/npm-g-nosudo.sh | sh
```

If you run the former command (rather than the wget version), the script will give you the option to fix your .bashrc or .zshrc file(s) automatically.

If you say "n", it will print the variables you need to enable you to fix manually.

If you say "y", you will need to source your corresponding file for your current environment vars to be updated.

If you run the command via wget, this changes the stdin for the script, so it doesn't run interactively and won't update your file.  It will echo out the variables you need to set near the end of the script output so you can copy these and add this to your environment manually.

## Important

After updating your environment files, you will need to [source](http://ss64.com/bash/source.html) the corresponding file before your npm binaries will be found in the current terminal session, e.g. for bash:
```
source ~/.bashrc
```
or just open an new terminal session.

## License

MIT © [Martin Meier](https://www.linkedin.com/in/me1er/)
