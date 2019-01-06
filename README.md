## Scrub

A Python script for bleeping out profanity in EPUBs. (Acknowledging that not everyone cares about that, but some people very much do.)

It has been tested on macOS but not Linux or Windows. If you come across an EPUB that it doesn't work with, let me know (or submit a PR).


### Installation and configuration

1. Copy the `scrub` script somewhere in your path and make sure it's executable.
2. Create a `.profanity` file in your home directory with a list of the words you'd like bleeped out, one per line. (If you want to change the path to this file, you can edit it at the top of `scrub`.) Words are bleeped in the order listed, so if there are longer variants (mother...), it's recommended to put those first.


### Usage

`scrub pottymouth.epub`

Which will save the scrubbed EPUB as `pottymouth-scrubbed.epub` and also output a count of how many of each word were scrubbed.

Bleeped words are all replaced with three bullet points.


### License


