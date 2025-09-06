# Installation

You can install the inflator using pipx.

`pipx install inflator`

You can now access the `inflate` command.
Verify that `inflate -h` shows a help menu like this:

```
usage: inflate [-h] [-i INPUT] [-V] [-L] {install,find,parse,toml,new,set} ...

Manage libraries for use in goboscript.

positional arguments:
  {install,find,parse,toml,new,set}
    install             Install a package
    find                Locate a package with a name/version/creator. Can also be used to list out installed pkgs. It is globbed.
    parse               Parse gstoml or iftoml file
    toml                Add an inflator.toml file to cwd
    new                 Create an (inflated) goboscript project
    set                 Set config in cookies.json

options:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        Set input directory for syncing. Default is cwd
  -V, --version         Get inflator version number
  -L, --log-folder      Get log folder

When called with no args: Sync libraries in the current directory.
```

## config

It is recommended to set up a [PAT](#config "Personal access token") for your
GitHub account.

### Setting up a PAT
This simply increases the rate limit for the GitHub api, from 60/hr to 5000/hr

1. Go [here](https://github.com/settings/tokens) and make a classic token with no permissions.
2. Copy token
3. Run `inflate set auth-token <value that you copied>`
4. Verify that the value is stored in `%appdata%/faretek/inflate/cookies.json` (windows) 
or `home/.faretek/inflate/cookies.json` (linux)
