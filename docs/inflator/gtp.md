# [GTP](https://github.com/inflated-goboscript/gtp)

> The goboscript table of packages

The GTP is inflator's package index.

!!! Question "What's a package index?"

    A package index is centralised, searchable repository of packages which package developers can use to
    distribute their packages.

    The GTP stores a [key-value mapping](https://github.com/inflated-goboscript/gtp/blob/main/gtp.json)
    of (inflated) goboscript packages, which are easy to install.

## Installing from the package index

Installing from the GTP is very easy. Simply:

`inflate install <name>`

So long as <name\> is not located in the current working directory, inflator will look it up on the GTP.
If it is found, it will install from the GitHub repository that the GTP registry refers to.

e.g. cmath -> [https://github.com/inflated-goboscript/cmath](https://github.com/inflated-goboscript/cmath)

## Registering a package on the package index

Register a package using [this issue template](https://github.com/inflated-goboscript/gtp/issues/new?template=register-package.yml).
A bot will automatically close the issue and add it to the registry, if valid, within a minute.

The bot's source code is available [here](https://github.com/inflated-goboscript/bfg). It's called the bfg.

!!! Info

    The bfg is currently hosted using [pythonanywhere](https://www.pythonanywhere.com/), which seems to be somewhat
    unstable. If the bot does not respond to your issue, ping me (@faretek1) on discord or GitHub, and I'll sort it out.
