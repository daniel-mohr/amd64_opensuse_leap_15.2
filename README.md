# run script in docker image opensuse/leap:15.2

This github action let you run a script/file inside the docker image
[opensuse/leap:15.2](https://hub.docker.com/r/opensuse/leap).

I will not maintain this repository. If you like it, please fork it and use
your own fork! This repository may break once!


## inputs


### `cmdfile`

The only parameter `cmdfile` is required and define the script to run.

For an example script, you can look at a trivial example [do](do).

The script is used directly from your repository and run on the root
of your repository.


## example usage

```
name: example

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  amd64_opensuse_leap_152_job_name:
    # https://github.com/daniel-mohr/amd64_opensuse_leap_15.2
    runs-on: ubuntu-latest
    name: opensuse leap 15.2
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: run my script in docker image
        uses: daniel-mohr/amd64_opensuse_leap_15.2@v0
        with:
          cmdfile: script_to_run
```

## repositories using this github action

I use this github action `daniel-mohr/amd64_opensuse_leap_15.2@v0` in a few
projects:

  * [check_my_github_actions](https://github.com/daniel-mohr/check_my_github_actions)
  * [pfu -- Python File Utilities](https://github.com/dlr-pa/pfu)


## copyright + license

Author: Daniel Mohr.

Date: 2021-08-26.

License: [BSD 3-Clause License](LICENSE.txt)
