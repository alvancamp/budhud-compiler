# budhud-compiler

> A Source engine HUD development tool to compile away as many #base and #include directives as possible. Designed for [budhud](https://github.com/rbjaxter/budhud).

## Usage

1. Grab the [latest release](https://github.com/alvancamp/budhud-compiler/releases/latest).
	- At this time, only Windows builds are provided. If you need builds for other platforms, consider building the program from source.
2. View the auto-generated help docs with `budhud-compiler.exe --help`:
	```
	budhud-compiler 1.7.0
	Copyright (C) 2022 Alex Van Camp

	  -i, --input                    Required. The specific files or directories to compile. Comma-separated.

	  -o, --output                   The files or directories to output to. Comma-separated. Prints to console if not provided. If input is a directory then output must also be a directory (or not yet exist).

	  -t, --trigger                  A list of files or directories which, when changed, will trigger a recompile, but which themselves aren't directly recompiled. If a trigger is provided, then the entire corresponding input directory will be recompiled on every change, instead of just the file(s) that changed being recompiled. Requires --watch.

	  -e, --errorOnMissing           (Default: false) If true, throws an error when a #base or #include file isn't present on disk.

	  -s, --silent                   (Default: false) If true, no information will be output to the console (aside from the finalized output if no output file is specified).

	  -m, --omitMissingDirectives    (Default: false) If true, directives which point to files that don't exist will be omitted from the final output.

	  -w, --watch                    (Default: false) If true, the input file or directory will be watched for changes and automatically recompiled to the specified output path. Ignored if no output paths are provided.

	  --help                         Display this help screen.

	  --version                      Display version information.
	```
3. Run the program with the desired options.

## Compliance

This program currently uses a modified version of [ValveKeyValue](https://github.com/SteamDatabase/ValveKeyValue). You can view the source code here: https://github.com/alvancamp/ValveKeyValue/tree/dev

## License

MIT
