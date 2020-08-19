# eml2mbox

This version of the script was forked from **[yardenac's updated version](https://github.com/yardenac/eml2mbox)**, and modified to support the `emlx` format on **macOS**. (Tested successfully on macOS Catalina 10.15.5.)

## Usage

```
[ruby] eml2mbx.rb [-a] [-c] [-h] [-l] [-m] [-s] [-yz] [emlpath [trgtmbx]]

Switches:
	-a assume all files are emails - ignore extensions
	-c Remove CRs (^M) appearing at end of lines (Unix)
	-f Act on a single .eml file, rather than an .eml dir
	-l Remove LFs appearing at beggining of lines (old Mac) - not tested
	-h Show help and exit
	-m Handle multiline From: headers (RFC822 phrase + routed_addr)
	-s Don't use standard mbox postmark formatting (for From_ line)
		This will force the use of original From and Date found in mail headers.
		Not recommended, unless you really have problems importing emls.
	-yz Use this to force the order of the year and timezone in date in the From_line from the default [timezone][year] to [year][timezone].

emlpath - Path of dir with eml files. Defaults to the current dir if not specified
trgtmbx - Name of the target mbox file. Defaults to "archive.mbox" in 'emlpath' 
```

## Original repo's ReadMe

This script was written by the person who runs this website: http://www.broobles.com

It did not work with recent Ruby versions, and did not have an Arch Linux package. So I am semi-forking it here. They are always welcome to unfork it and take the credit. :)

It can handle files that end in EML or MAI (aka RFC 822) such as the ones stored by Mail Enable. It turns these into mbox files.
