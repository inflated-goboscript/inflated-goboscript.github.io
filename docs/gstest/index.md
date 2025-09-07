# [gstest](https://github.com/inflated-goboscript/gstest)

> gstest allows you to run automated tests on goboscript projects

!!! Note
    
    - It's currently rather slow (~2mins) because of playright.
    - It's probably possible to speed this up using docker but I do not know how to use it.
    - If you know how to and are willing to, please do open a [pull request](https://github.com/inflated-goboscript/gstest/pulls)!

## Usage

!!! Warning

    This assumes:
    - You are using [inflator](../inflator) to handle dependencies
    - You have a `/test/` [inflator project](../inflator/usage/getting%20started/#:~:text=new%20project%20with%20inflator)

Add `.github/workflows/gstest.yml` to your GitHub repository:

```yaml
name: Run /test/

on:
  pull_request:
    branches: ['main']
  push:
    branches: ['main']
  release:
    types: [prereleased, published]
  workflow_dispatch:

jobs:
  tests:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
    - uses: inflated-goboscript/gstest@v0.0.4  # change this to the most recent version
```

!!! Note "gstest dependencies"

    These are some of the dependencies installed by the gstest action:

    - goboscript
    - inflator
    - TW-CLI
        - playwright
