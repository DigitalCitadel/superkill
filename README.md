# Superkill

Superkill is a shell command that kills a process by a partial name.

## Installation

In both methods, you'll need to start by cloning down this repo to your local computer.

### With Symlink (recommended)

> This method is recommended as you'll be able to easily update superkill by running a git pull

- Move the cloned repo to a good place to perminantly keep the repo
- Symlink the superkill file into your `$PATH` (usually /usr/local/bin)

## Without Symlink

Without a symlink, you can simply move the superkill file to somewhere in your `$PATH`.

## Usage

Using superkill is very simple:

```sh
superkill $partial_process_name
```

If you'd like you kill a process that has a space in the name, make sure to quote the process name

```sh
superkill "Android Studio"
```

After running superkill you will be prompted with one of two things.

An error in the event no process was found:

```
No process found
```

A prompt asking if you'd like to kill the process in the event a process was found:
```
kill /Applications/Android Studio.app/Contents/MacOS/studio ? (y/n):
```

Answering `y` (case insensitive) will kill the process while logging:

```
>> killing /Applications/Android Studio.app/Contents/MacOS/studio
```

Any other response will exit silently and not kill anything.

## License

[MIT](license.md)
