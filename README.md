# `node-venv`

At the moment all this script does is update your PATH variable to include
`./node_modules/.bin`. Works similarly to (but worse than) python's `venv`.

## Installation

Copy-paste this command into your shell to install the script to `~/.local/bin`.
You can put it anywhere you like as long as it's in your shell's `PATH`.
```
curl -s https://raw.githubusercontent.com/jaf7C7/node-venv/master/node-venv -o ~/.local/bin/node-venv && chmod +x $_
```

Check it's installed properly
```
$ type node-venv
node-venv is /home/jfox/.local/bin/node-venv
```

## Usage

```
$ # `cd` to the root of your chosen project and run the command
$ cd ~/Projects/foo-project && node-venv
$
$ # Source the 'activate' script to update your PATH
$ . node_modules/.bin/activate
$
$ # Check your new path value
$ echo $PATH
/home/jfox/Projects/foo-project/node_modules/.bin:/home/jfox/.local/bin: # ...
$
$ # Install a package
$ npm install browser-sync
# ...
$
$ # Check the packages executable is in your PATH
$ type browser-sync
browser-sync is /home/jfox/Projects/foo-project/node_modules/.bin/browser-sync
$
$ # When you're done just type 'deactivate'
$ deactivate
$ echo $PATH
/home/jfox/.local/bin:/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin
