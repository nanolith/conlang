constructed language
====================

I need a constructed language for annotation. Specifically, I should be able to
train a recognizer on this language and run it using an edge computing node.
This should be able to run offline, anywhere and any place I am.

As of this writing, this presents some challenges. Recognizers are limited by
the size of neural coprocessors (e.g. TPUs) that are available. Further,
constraints such as power budget further limit the complexity of a language that
can be recognized.

This document captures ideas and begins sketching out what this language looks
like.
