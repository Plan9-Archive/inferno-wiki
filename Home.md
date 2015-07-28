# Inferno and Limbo

Inferno provides an operating system environment for applications written in the concurrent programming
language Limbo.

## Pages

* [Inferno and Limbo Plans](InfernoAndLimboPlans.md)
* [Project Suggestions, including GSoC Projects](Project_Suggestions.md)
* [Advice for GSoC Project Applicants](Project_Applicants.md)

## Wiki features

This wiki uses the [Markdown](http://daringfireball.net/projects/markdown/) syntax.

The wiki itself is actually a mercurial repository, which means you can clone it, edit it locally/offline, add images or any other file type, and push it back to us. It will be live immediately.

Go ahead and try:

```
$ hg clone https://inferno-os@bitbucket.org/inferno-os/inferno-os/wiki
```

Wiki pages are normal files, with the .md extension. You can edit them locally, as well as creating new ones.

## Syntax highlighting


You can also highlight snippets of text (we use the excellent [Pygments][] library).

[Pygments]: http://pygments.org/


Here's an example of some Limbo code:

```
#!limbo

implement Hello;

include "sys.m";
	sys: Sys;
include "draw.m";

Hello: module
{
	init:	fn(ctxt: ref Draw->Context, argv: list of string);
};

init(ctxt: ref Draw->Context, argv: list of string)
{
	sys = load Sys Sys->PATH;
	sys->print("hello, world\n");
}
```


You can check out the source of this page to see how that's done, and make sure to bookmark [the vast library of Pygment lexers][lexers], we accept the 'short name' or the 'mimetype' of anything in there.
[lexers]: http://pygments.org/docs/lexers/


Have fun!
