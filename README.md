# budhud-compiler

> A tool to compile away as many #base and #include directives as possible.

## Usage

> 💡 This tool currently only takes a single file as input. If you need to compile multiple files, consider writing a shell script that iterates over them and invokes `budhud-compiler` on each of them.

1. Grab the [latest release](https://github.com/alvancamp/budhud-compiler/releases).
	- At this time, only Windows builds are provided. If you need builds for other platforms, consider building the program from source.
2. View the auto-generated help docs with `budhud-compiler.exe --help`:
	```
	budhud-compiler 1.0.0
	Copyright (C) 2022 budhud-compiler

	-i, --input               Required. The specific file to compile.

	-o, --output              (Default: ) The file to output to. Prints to console if not provided.

	-m, --skipMissingFiles    (Default: true) If false, throws an error when a #base or #include file isn't present on disk.

	-s, --silent              (Default: false) If true, no information will be output to the console (aside from the finalized output if no output file is specified).

	--help                    Display this help screen.

	--version                 Display version information.
	```
3. Run the program with the desired options.

## Compliance

This program currently uses a modified version of [ValveKeyValue](https://github.com/SteamDatabase/ValveKeyValue). You can view the source code here: https://github.com/alvancamp/ValveKeyValue/tree/dev

## License

MIT
