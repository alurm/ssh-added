Bernstein chained ssh-add

Rationale

Ssh-agent already allows bernstein chained form, but ssh-add, for some reason, doesn't. Thus, it's not possible to do the following:

	ssh-agent ssh-add path/to/key git push

This utility makes it possible:

	ssh-agent ssh_added path/to/key git push

In fact, this is almost exactly how this repository was pushed to GitHub.

This utility is not complicated, it's only a couple of lines of code. Another example:

	ssh-agent ssh_added path/to/key echo Hello, world

This utility also uses -q flag with ssh-add to avoid extra noise.

Installation

	Copy ssh_added script somewhere in your path.

License: MIT.

References

Bernstein chaining: https://en.wikipedia.org/wiki/Chain_loading
Example of Bernstein chaining: https://skarnet.org/software/execline/grammar.html
More Bernstein chaining: https://www.catb.org/~esr/writings/taoup/html/ch06s06.html
