## Scrub

A Python script for bleeping out profanity in EPUBs. (Acknowledging that not everyone cares about that, but some people very much do.)

It has been tested on macOS but not Linux or Windows. If you come across an EPUB that it doesn't work with, let me know (or submit a PR).


### Installation and configuration

1. Copy the `scrub` script somewhere in your path and make sure it's executable.
2. Create a `.profanity` file in your home directory with a list of the words you'd like bleeped out, one per line. (If you want to change the path to this file, you can edit it at the top of `scrub`.) Words are bleeped in the order listed. Labels for each bleeped entry can be added after a tab on the line (see the example). Also, `.*word*.` will compile to `\b\w*?word\w*?\b`, as an easy shorthand to handle variants (wording, prefixworders, etc.).

#### Example profanity file

```
.*bleep*.   b-bomb
scraps  s-bomb
crikey
```

#### Example output

```
94 files scrubbed.
b-bomb: 32
s-bomb: 0
c•••••: 3
```


### Usage

`scrub pottymouth.epub`

Which will save the scrubbed EPUB as `pottymouth-scrubbed.epub` and also output a count of how many of each word were scrubbed.

Bleeped words are all replaced in the text with three bullet points.


### License

Copyright 2019 Ben Crowder.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
