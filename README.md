# launcher

The super simple process launcher

## Installation

Do you have python installed?  Good.  Now just download the script to
your bin, you nerd.

```shell
wget -O ~/bin/launcher https://raw.githubusercontent.com/arecker/launcher/main/launcher
chmod +x ~/bin/launcher
```

## Running

Point it at a config file and watch this baby purr.

```shell
launcher --config ~/launcher.conf
```

Nosy types can run the program with verbose logging turned on.

```shell
launcher --verbose --config ~/launcher.conf
```

## Configuration

Configure jobs with a regular-ass config file.

```conf
[blog]
directory = ~/src/blog
command = $HOME/.pyenv/shims/python -m src serve
envfile = ~/envs/blog.env  # optional
```

### `envfile`

Load environment variables into your job by specifying a path to an
environment file.  The file should look something like this:

    TEST_VARIABLE="hello"
    MY_FAVORITE_NUMBER="1"

Of course quotes are optional, but how lazy can you be?

## Examples

Take it for a spin using the provided examples.

```bash
./launcher --config examples/launcher.conf
```
