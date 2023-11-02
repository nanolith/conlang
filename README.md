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

Usage modes
-----------

I care about three usage modes: conversations, descriptions, and commands.
Command mode is meant for controlling devices or for devices to instruct a user.
Description mode allows a device to take dictation of information that is useful
to a user. Conversation mode allows multiple users or devices to exchange
information.

Proto-Pronouns and Discriminators
---------------------------------

There are three proto-pronouns, representing me, you, and other. Proto-pronouns
may be used directly, at which point, specific descriminators should be
considered vague and elided. Discriminators build on these proto-pronouns by
making some description of which "me", "you", or "other" is being described.
Example discriminators are singular/plural, masculine, feminine, that/this, or
adjective-modifier.
