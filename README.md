# linuxify

Transparently transform macOS into a fresh GNU/Linux experience by

- installing missing GNU programs
- updating outdated GNU programs
- replacing pre-installed BSD programs with their preferred GNU implementation
- installing other programs common among popular GNU/Linux distributions

## Installation

Clone the repository and make the script executable:

````bash
$ git clone git@github.com:fabiomaia/linuxify.git
$ cd linuxify/
$ chmod +x linuxify.sh
```

Optionally make the script available in your `$PATH`:

```bash
$ ln -s linuxify.sh /usr/local/bin/linuxify
```

Run the install procedure:

```bash
$ linuxify install
```

Source the created `~/.macos` file from `~/.bashrc`, `~/.bash_profile` or similar:

```bash
[[ "$OSTYPE" =~ ^darwin ]] && source ~/.macos
```

## Updating

In case `linuxify` is significantly updated and you wish to stay up to date, it is recommended that you:

1. Run the uninstall procedure
2. Pull the latest code or otherwise obtain a fresh copy of the code
3. Run the install procedure again

```bash
$ linuxify uninstall
$ # ...
$ git pull
$ linuxify install
```

## Uninstallation

If you need to undo the changes made by `linuxify`, run the uninstall procedure:

```bash
linuxify uninstall
```

Remove the `.macos` source from `~/.bashrc`, `~/.bash_profile` or similar.